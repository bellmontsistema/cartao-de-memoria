---
title: Requisição Axios com Hook + TypeScript
description: Criando um hook com requisição axios reutilizável para consumo de api
date: 2022-02-14 08:13:51
thumbnail: data:image/png;base64,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
category: NextJS
background: "#000000"
---
1. Instalar o Axion `yarn add axios`
2. `Criar uma pasta `Hook
3. `Criar um arquivo com o nome `useFetch.tsx

   Criando o Hook

   ```tsx
   import axios, { AxiosRequestConfig } from 'axios'
   import { useEffect, useState } from 'react'

   const api = axios.create({
     baseURL: 'https://api.github.com'
   })

   export function useFetch<T = unknown>(
     url: string,
     options?: AxiosRequestConfig
   ) {
     const [data, setData] = useState<T | null>(null)
     const [isFetching, setIsFetching] = useState(true)
     const [error, setError] = useState(null)

     useEffect(() => {
       api
         .get(url, options)
         .then((response) => {
           setData(response.data)
         })
         .catch((err) => {
           setError(err)
         })
         .finally(() => {
           setIsFetching(false)
         })
     }, [])

     return { data, isFetching, error }
   }

   ```

   Consumindo o Hook

   ```tsx
   import { useFetch } from 'hook/useFetch'
   import React from 'react'

   type Repositories = {
     full_name: string
     description: string
   }

   import * as S from './styled'

   export const FetchAxios = () => {
     const { data: repositories, isFetching } = useFetch<Repositories[]>(
       '/users/bellmontsistema/repos'
     )

     return (
       <S.Section>
         <S.Content>
           {isFetching && <p>Carregando...</p>}
           <ul>
             {repositories?.map((item, i) => (
               <li key={i}>
                 <strong>{item.full_name}</strong>
                 <p>{item.description}</p>
               </li>
             ))}
           </ul>
         </S.Content>
       </S.Section>
     )
   }

   export default FetchAxios

   ```

   Dicas

   ```tsx
   const api = axios.create({
     baseURL: 'https://api.github.com'
   })

   //

   É a base url da requisição
   basta tirar o nome axios e trocar para api
   ```

   ```tsx
    //hook/useFetch
   const [data, setData] = useState<T | null>(null)

   É a resposata da api

   pode ser mudado o nome da hora da requisição

   //componente
             data mudado para repositories
     const { data: repositories, isFetching } = useFetch<Repositories[]>(
       '/users/bellmontsistema/repos'
     )
   ```

   ```tsx
    //hook/useFetch
   const [isFetching, setIsFetching] = useState(true)
    
    Para exibir uma mensagem de carregamento ou um componentes
    na tela ,
      
   //Componente
      {isFetching && <p>Carregando...</p>}
     
    
    
   ```

   ```tsx
    //hook/useFetch
   const [error, setError] = useState(null)

   Para exibir alguma mensagem de erro na tela ou no console
   ```