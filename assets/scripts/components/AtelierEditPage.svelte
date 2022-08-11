<script>
    import fm from 'front-matter'

    export let page;
    export let fileContent;
    export let onPageEdit;

    throw `TODO 
        await filecontent and put a spinner

        await fileContent
        parse the text 
        and split title and content
    `
    
    const onSubmit = (e) => {
        e.preventDefault()
        onPageEdit(title, content)
    }
    
    </script>
    
    <section class="screen">
        <h3>Création d'une page</h3>
    
        <form on:submit={onSubmit}>
            <div>
                <label for="title">Titre</label>
                <input bind:value={title} type="text" id="title">
            </div>
            <p>Attention, si le titre contient <code>/</code>, <code>#</code> ou <code>?</code>, ça peut ne pas marcher
            </p>
    
            <div>
                <label for="content">Contenu</label>
                <textarea bind:value={content} id="content" cols="30" rows="10"></textarea>
            </div>
            <button type="submit">Publier la page</button>
        </form>
    </section>