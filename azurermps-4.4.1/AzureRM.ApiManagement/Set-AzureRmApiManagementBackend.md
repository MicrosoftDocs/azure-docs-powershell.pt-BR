---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610221"
---
# <span data-ttu-id="76ced-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="76ced-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="76ced-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76ced-102">SYNOPSIS</span></span>
<span data-ttu-id="76ced-103">Atualiza um back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76ced-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76ced-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76ced-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76ced-105">DESCRIPTION</span></span>
<span data-ttu-id="76ced-106">Atualiza um back-end existente no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="76ced-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="76ced-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76ced-107">EXAMPLES</span></span>

### <span data-ttu-id="76ced-108">Atualiza a descrição do back-end 123</span><span class="sxs-lookup"><span data-stu-id="76ced-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="76ced-109">OS</span><span class="sxs-lookup"><span data-stu-id="76ced-109">PARAMETERS</span></span>

### <span data-ttu-id="76ced-110">-Backid</span><span class="sxs-lookup"><span data-stu-id="76ced-110">-BackendId</span></span>
<span data-ttu-id="76ced-111">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-111">Identifier of new backend.</span></span>
<span data-ttu-id="76ced-112">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="76ced-112">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="76ced-113">-Context</span></span>
<span data-ttu-id="76ced-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="76ced-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="76ced-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="76ced-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="76ced-116">-Credential</span></span>
<span data-ttu-id="76ced-117">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="76ced-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76ced-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="76ced-119">-Description</span></span>
<span data-ttu-id="76ced-120">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-120">Backend Description.</span></span>
<span data-ttu-id="76ced-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76ced-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76ced-122">-PassThru</span></span>
<span data-ttu-id="76ced-123">Indica que esse cmdlet retorna o  **PsApiManagementBackend** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="76ced-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-124">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="76ced-124">-Protocol</span></span>
<span data-ttu-id="76ced-125">Protocolo de comunicação back-end (http ou SOAP).</span><span class="sxs-lookup"><span data-stu-id="76ced-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="76ced-126">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="76ced-126">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-127">-Proxy</span><span class="sxs-lookup"><span data-stu-id="76ced-127">-Proxy</span></span>
<span data-ttu-id="76ced-128">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="76ced-129">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76ced-129">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76ced-130">-ResourceId</span></span>
<span data-ttu-id="76ced-131">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="76ced-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="76ced-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76ced-132">This parameter is optional.</span></span>
<span data-ttu-id="76ced-133">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="76ced-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="76ced-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="76ced-135">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="76ced-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76ced-136">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="76ced-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="76ced-138">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="76ced-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76ced-139">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-140">-Título</span><span class="sxs-lookup"><span data-stu-id="76ced-140">-Title</span></span>
<span data-ttu-id="76ced-141">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-141">Backend Title.</span></span>
<span data-ttu-id="76ced-142">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76ced-142">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-143">-URL</span><span class="sxs-lookup"><span data-stu-id="76ced-143">-Url</span></span>
<span data-ttu-id="76ced-144">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="76ced-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="76ced-145">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76ced-145">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76ced-146">-Confirm</span></span>
<span data-ttu-id="76ced-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76ced-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76ced-148">-WhatIf</span></span>
<span data-ttu-id="76ced-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76ced-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76ced-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76ced-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ced-151">-DefaultProfile</span></span>
<span data-ttu-id="76ced-152">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76ced-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ced-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ced-153">CommonParameters</span></span>
<span data-ttu-id="76ced-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ced-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ced-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ced-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ced-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76ced-156">INPUTS</span></span>

## <span data-ttu-id="76ced-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76ced-157">OUTPUTS</span></span>

### <span data-ttu-id="76ced-158">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="76ced-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="76ced-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76ced-159">NOTES</span></span>

## <span data-ttu-id="76ced-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76ced-160">RELATED LINKS</span></span>

[<span data-ttu-id="76ced-161">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="76ced-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="76ced-162">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="76ced-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="76ced-163">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="76ced-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="76ced-164">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="76ced-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="76ced-165">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="76ced-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
