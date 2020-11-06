---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430543"
---
# <span data-ttu-id="d8401-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d8401-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d8401-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8401-102">SYNOPSIS</span></span>
<span data-ttu-id="d8401-103">Atualiza um back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8401-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8401-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8401-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8401-105">DESCRIPTION</span></span>
<span data-ttu-id="d8401-106">Atualiza um back-end existente no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="d8401-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="d8401-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8401-107">EXAMPLES</span></span>

### <span data-ttu-id="d8401-108">Atualiza a descrição do back-end 123</span><span class="sxs-lookup"><span data-stu-id="d8401-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="d8401-109">OS</span><span class="sxs-lookup"><span data-stu-id="d8401-109">PARAMETERS</span></span>

### <span data-ttu-id="d8401-110">-Backid</span><span class="sxs-lookup"><span data-stu-id="d8401-110">-BackendId</span></span>
<span data-ttu-id="d8401-111">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-111">Identifier of new backend.</span></span>
<span data-ttu-id="d8401-112">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d8401-112">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d8401-113">-Context</span></span>
<span data-ttu-id="d8401-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d8401-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d8401-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d8401-115">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="d8401-116">-Credential</span></span>
<span data-ttu-id="d8401-117">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="d8401-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d8401-118">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8401-119">-DefaultProfile</span></span>
<span data-ttu-id="d8401-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8401-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d8401-121">-Description</span></span>
<span data-ttu-id="d8401-122">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-122">Backend Description.</span></span>
<span data-ttu-id="d8401-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d8401-123">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8401-124">-PassThru</span></span>
<span data-ttu-id="d8401-125">Indica que esse cmdlet retorna o  **PsApiManagementBackend** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d8401-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-126">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="d8401-126">-Protocol</span></span>
<span data-ttu-id="d8401-127">Protocolo de comunicação back-end (http ou SOAP).</span><span class="sxs-lookup"><span data-stu-id="d8401-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="d8401-128">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="d8401-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="d8401-129">-Proxy</span></span>
<span data-ttu-id="d8401-130">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="d8401-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d8401-131">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8401-132">-ResourceId</span></span>
<span data-ttu-id="d8401-133">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="d8401-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="d8401-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d8401-134">This parameter is optional.</span></span>
<span data-ttu-id="d8401-135">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="d8401-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="d8401-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="d8401-137">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="d8401-138">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d8401-138">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="d8401-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="d8401-140">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="d8401-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d8401-141">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-142">-Título</span><span class="sxs-lookup"><span data-stu-id="d8401-142">-Title</span></span>
<span data-ttu-id="d8401-143">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-143">Backend Title.</span></span>
<span data-ttu-id="d8401-144">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d8401-144">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-145">-URL</span><span class="sxs-lookup"><span data-stu-id="d8401-145">-Url</span></span>
<span data-ttu-id="d8401-146">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="d8401-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="d8401-147">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d8401-147">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8401-148">-Confirm</span></span>
<span data-ttu-id="d8401-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8401-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8401-150">-WhatIf</span></span>
<span data-ttu-id="d8401-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8401-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8401-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8401-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8401-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8401-153">CommonParameters</span></span>
<span data-ttu-id="d8401-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8401-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8401-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8401-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8401-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8401-156">INPUTS</span></span>

### <span data-ttu-id="d8401-157">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d8401-157">None</span></span>
<span data-ttu-id="d8401-158">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d8401-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8401-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8401-159">OUTPUTS</span></span>

### <span data-ttu-id="d8401-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d8401-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d8401-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8401-161">NOTES</span></span>

## <span data-ttu-id="d8401-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8401-162">RELATED LINKS</span></span>

[<span data-ttu-id="d8401-163">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d8401-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d8401-164">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d8401-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d8401-165">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d8401-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d8401-166">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d8401-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d8401-167">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d8401-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
