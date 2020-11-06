---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431239"
---
# <span data-ttu-id="75b48-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b48-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="75b48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75b48-102">SYNOPSIS</span></span>
<span data-ttu-id="75b48-103">Cria uma nova entidade back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75b48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75b48-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75b48-105">DESCRIPTION</span></span>
<span data-ttu-id="75b48-106">Cria uma nova entidade back-end no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="75b48-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="75b48-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75b48-107">EXAMPLES</span></span>

### <span data-ttu-id="75b48-108">Criar back-end 123 com um esquema de autorização básico</span><span class="sxs-lookup"><span data-stu-id="75b48-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="75b48-109">Cria um novo back-end</span><span class="sxs-lookup"><span data-stu-id="75b48-109">Creates a new Backend</span></span>

## <span data-ttu-id="75b48-110">OS</span><span class="sxs-lookup"><span data-stu-id="75b48-110">PARAMETERS</span></span>

### <span data-ttu-id="75b48-111">-Backid</span><span class="sxs-lookup"><span data-stu-id="75b48-111">-BackendId</span></span>
<span data-ttu-id="75b48-112">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-112">Identifier of new backend.</span></span>
<span data-ttu-id="75b48-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75b48-113">This parameter is optional.</span></span>
<span data-ttu-id="75b48-114">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="75b48-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="75b48-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="75b48-115">-Context</span></span>
<span data-ttu-id="75b48-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="75b48-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="75b48-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="75b48-117">This parameter is required.</span></span>

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

### <span data-ttu-id="75b48-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="75b48-118">-Credential</span></span>
<span data-ttu-id="75b48-119">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="75b48-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75b48-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="75b48-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="75b48-121">-Description</span></span>
<span data-ttu-id="75b48-122">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-122">Backend Description.</span></span>
<span data-ttu-id="75b48-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75b48-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="75b48-124">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="75b48-124">-Protocol</span></span>
<span data-ttu-id="75b48-125">Protocolo de comunicação back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-125">Backend Communication protocol.</span></span>
<span data-ttu-id="75b48-126">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="75b48-126">This parameter is required.</span></span>
<span data-ttu-id="75b48-127">Os valores válidos são ' http ' e ' SOAP '.</span><span class="sxs-lookup"><span data-stu-id="75b48-127">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b48-128">-Proxy</span><span class="sxs-lookup"><span data-stu-id="75b48-128">-Proxy</span></span>
<span data-ttu-id="75b48-129">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="75b48-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75b48-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="75b48-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75b48-131">-ResourceId</span></span>
<span data-ttu-id="75b48-132">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="75b48-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="75b48-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75b48-133">This parameter is optional.</span></span>
<span data-ttu-id="75b48-134">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="75b48-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="75b48-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="75b48-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="75b48-136">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="75b48-137">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75b48-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="75b48-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="75b48-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="75b48-139">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="75b48-140">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75b48-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="75b48-141">-Título</span><span class="sxs-lookup"><span data-stu-id="75b48-141">-Title</span></span>
<span data-ttu-id="75b48-142">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-142">Backend Title.</span></span>
<span data-ttu-id="75b48-143">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75b48-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="75b48-144">-URL</span><span class="sxs-lookup"><span data-stu-id="75b48-144">-Url</span></span>
<span data-ttu-id="75b48-145">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="75b48-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="75b48-146">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="75b48-146">This parameter is required.</span></span>

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

### <span data-ttu-id="75b48-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75b48-147">-Confirm</span></span>
<span data-ttu-id="75b48-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75b48-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b48-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b48-149">-WhatIf</span></span>
<span data-ttu-id="75b48-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75b48-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75b48-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75b48-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b48-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b48-152">-DefaultProfile</span></span>
<span data-ttu-id="75b48-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75b48-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75b48-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b48-154">CommonParameters</span></span>
<span data-ttu-id="75b48-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b48-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b48-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b48-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b48-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75b48-157">INPUTS</span></span>

## <span data-ttu-id="75b48-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75b48-158">OUTPUTS</span></span>

### <span data-ttu-id="75b48-159">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b48-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="75b48-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75b48-160">NOTES</span></span>

## <span data-ttu-id="75b48-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75b48-161">RELATED LINKS</span></span>

[<span data-ttu-id="75b48-162">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b48-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="75b48-163">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="75b48-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="75b48-164">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="75b48-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="75b48-165">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b48-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="75b48-166">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b48-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

