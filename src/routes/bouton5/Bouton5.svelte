<script>
    import { supabase } from "../../supabaseClient";

    import { createForm } from "svelte-forms-lib";
    import * as yup from "yup";

    import { TextInput, TextArea, Button, FormGroup, Form, InlineNotification } from "carbon-components-svelte";

    const validationSchema = yup.object().shape({
        name: yup.string().required('Please enter a name'),
        email: yup.string().email().required('Please enter a valid email'),
        message: yup.string().required('Please enter a message')
    });

    /**
     * @type {boolean | null}
     */
    let apiResult = null;

    const { form, errors, handleChange, handleSubmit, isSubmitting, handleReset } = createForm({
        initialValues: { name: "", email: "", message: "" },
        validationSchema: validationSchema,
        onSubmit: async values => {

            try {
                var result = await supabase.from("contact").insert(values);
                if (result.status === 201) {
                    apiResult = true;
                } else {
                    apiResult = false;
                }

            } catch (ex) {
                console.log(ex)
                apiResult = false;
            }

            //handleReset();
      }
    });

</script>
<div class="page bg-gradient-to-r from-violet-200  ">

    <h2 class="text-3xl font-extrabold py-18 mt-48 text-center mb-2">Merci de nous faire un retour de votre expérience!</h2>
    <p class="text-gray-900 font-semibold text-center ml-4 mr-4 mb-4 ">Vous pouvez inscrire vos coordonnées et nous faire un retour sur votre expérience "Info taxecarbone"! Nous reviendrons vers vous très vite, merci!</p> <br/><br/>

    {#if apiResult != null}

        {#if apiResult === true}
        <InlineNotification
            lowContrast
            kind="success"
            title="Success:"
            subtitle="Your message has been received"
        />
        {:else}
        <InlineNotification lowContrast kind="error"
            title="Error:"
            subtitle="An internal server error occurred."
        />

        {/if}    
    {/if}
    <Form on:submit={handleSubmit}>

        <FormGroup>
            <TextInput  labelText="Votre nom" name="name" 
                on:change={handleChange} bind:value={$form.name}
                invalid={$errors.name.length > 0} invalidText={$errors.name}/>
        </FormGroup>

        <FormGroup>
            <TextInput  labelText="Votre email" name="email" type="email" 
                on:change={handleChange} bind:value={$form.email}
                invalid={$errors.email.length > 0} invalidText={$errors.email}/>
        </FormGroup>


        <FormGroup>
            <TextArea labelText="Vos suggestions!" name="message" type="textarea"
                on:change={handleChange} bind:value={$form.message}
                invalid={$errors.message.length > 0} invalidText={$errors.message}/>
        </FormGroup>


        <Button class="bg-slate-600 text-3xl font-extrabold py-7 text-center mb-2 place-items-center px-7"  type="submit" disabled={$isSubmitting}>Envoyer le formulaire</Button>
    </Form>
</div>

<style>
    .page {
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>
