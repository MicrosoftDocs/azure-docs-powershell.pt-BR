---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440901"
---
# <span data-ttu-id="e924b-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e924b-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="e924b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e924b-102">SYNOPSIS</span></span>
<span data-ttu-id="e924b-103">Cria uma nova entidade back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e924b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e924b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e924b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e924b-105">DESCRIPTION</span></span>
<span data-ttu-id="e924b-106">Cria uma nova entidade back-end no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e924b-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="e924b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e924b-107">EXAMPLES</span></span>

### <span data-ttu-id="e924b-108">Criar back-end 123 com um esquema de autorização básico</span><span class="sxs-lookup"><span data-stu-id="e924b-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="e924b-109">Cria um novo back-end</span><span class="sxs-lookup"><span data-stu-id="e924b-109">Creates a new Backend</span></span>

## <span data-ttu-id="e924b-110">OS</span><span class="sxs-lookup"><span data-stu-id="e924b-110">PARAMETERS</span></span>

### <span data-ttu-id="e924b-111">-Backid</span><span class="sxs-lookup"><span data-stu-id="e924b-111">-BackendId</span></span>
<span data-ttu-id="e924b-112">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-112">Identifier of new backend.</span></span>
<span data-ttu-id="e924b-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e924b-113">This parameter is optional.</span></span>
<span data-ttu-id="e924b-114">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="e924b-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="e924b-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e924b-115">-Context</span></span>
<span data-ttu-id="e924b-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e924b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e924b-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e924b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="e924b-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="e924b-118">-Credential</span></span>
<span data-ttu-id="e924b-119">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="e924b-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e924b-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="e924b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e924b-121">-DefaultProfile</span></span>
<span data-ttu-id="e924b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e924b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e924b-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e924b-123">-Description</span></span>
<span data-ttu-id="e924b-124">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-124">Backend Description.</span></span>
<span data-ttu-id="e924b-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e924b-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="e924b-126">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="e924b-126">-Protocol</span></span>
<span data-ttu-id="e924b-127">Protocolo de comunicação back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-127">Backend Communication protocol.</span></span>
<span data-ttu-id="e924b-128">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e924b-128">This parameter is required.</span></span>
<span data-ttu-id="e924b-129">Os valores válidos são ' http ' e ' SOAP '.</span><span class="sxs-lookup"><span data-stu-id="e924b-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e924b-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="e924b-130">-Proxy</span></span>
<span data-ttu-id="e924b-131">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="e924b-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e924b-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="e924b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e924b-133">-ResourceId</span></span>
<span data-ttu-id="e924b-134">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="e924b-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="e924b-135">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e924b-135">This parameter is optional.</span></span>
<span data-ttu-id="e924b-136">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="e924b-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="e924b-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="e924b-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="e924b-138">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="e924b-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e924b-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="e924b-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="e924b-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="e924b-141">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="e924b-142">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e924b-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="e924b-143">-Título</span><span class="sxs-lookup"><span data-stu-id="e924b-143">-Title</span></span>
<span data-ttu-id="e924b-144">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-144">Backend Title.</span></span>
<span data-ttu-id="e924b-145">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e924b-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="e924b-146">-URL</span><span class="sxs-lookup"><span data-stu-id="e924b-146">-Url</span></span>
<span data-ttu-id="e924b-147">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="e924b-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="e924b-148">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e924b-148">This parameter is required.</span></span>

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

### <span data-ttu-id="e924b-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e924b-149">-Confirm</span></span>
<span data-ttu-id="e924b-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e924b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e924b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e924b-151">-WhatIf</span></span>
<span data-ttu-id="e924b-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e924b-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e924b-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e924b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e924b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e924b-154">CommonParameters</span></span>
<span data-ttu-id="e924b-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e924b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e924b-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e924b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e924b-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e924b-157">INPUTS</span></span>

### <span data-ttu-id="e924b-158">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e924b-158">None</span></span>
<span data-ttu-id="e924b-159">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e924b-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e924b-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e924b-160">OUTPUTS</span></span>

### <span data-ttu-id="e924b-161">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e924b-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e924b-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e924b-162">NOTES</span></span>

## <span data-ttu-id="e924b-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e924b-163">RELATED LINKS</span></span>

[<span data-ttu-id="e924b-164">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e924b-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="e924b-165">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e924b-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="e924b-166">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e924b-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="e924b-167">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e924b-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e924b-168">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e924b-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

