---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955835"
---
# <span data-ttu-id="e432d-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e432d-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="e432d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e432d-102">SYNOPSIS</span></span>
<span data-ttu-id="e432d-103">Cria uma nova entidade back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="e432d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e432d-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e432d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e432d-105">DESCRIPTION</span></span>
<span data-ttu-id="e432d-106">Cria uma nova entidade back-end no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e432d-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="e432d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e432d-107">EXAMPLES</span></span>

### <span data-ttu-id="e432d-108">Exemplo 1: criar back-end 123 com um esquema de autorização básico</span><span class="sxs-lookup"><span data-stu-id="e432d-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="e432d-109">Cria um novo back-end</span><span class="sxs-lookup"><span data-stu-id="e432d-109">Creates a new Backend</span></span>

## <span data-ttu-id="e432d-110">OS</span><span class="sxs-lookup"><span data-stu-id="e432d-110">PARAMETERS</span></span>

### <span data-ttu-id="e432d-111">-Backid</span><span class="sxs-lookup"><span data-stu-id="e432d-111">-BackendId</span></span>
<span data-ttu-id="e432d-112">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-112">Identifier of new backend.</span></span>
<span data-ttu-id="e432d-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-113">This parameter is optional.</span></span>
<span data-ttu-id="e432d-114">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="e432d-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="e432d-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e432d-115">-Context</span></span>
<span data-ttu-id="e432d-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e432d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e432d-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e432d-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e432d-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="e432d-118">-Credential</span></span>
<span data-ttu-id="e432d-119">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="e432d-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="e432d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e432d-121">-DefaultProfile</span></span>
<span data-ttu-id="e432d-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e432d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e432d-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e432d-123">-Description</span></span>
<span data-ttu-id="e432d-124">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-124">Backend Description.</span></span>
<span data-ttu-id="e432d-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="e432d-126">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="e432d-126">-Protocol</span></span>
<span data-ttu-id="e432d-127">Protocolo de comunicação back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-127">Backend Communication protocol.</span></span>
<span data-ttu-id="e432d-128">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e432d-128">This parameter is required.</span></span>
<span data-ttu-id="e432d-129">Os valores válidos são ' http ' e ' SOAP '.</span><span class="sxs-lookup"><span data-stu-id="e432d-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="e432d-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="e432d-130">-Proxy</span></span>
<span data-ttu-id="e432d-131">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="e432d-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="e432d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e432d-133">-ResourceId</span></span>
<span data-ttu-id="e432d-134">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="e432d-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="e432d-135">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-135">This parameter is optional.</span></span>
<span data-ttu-id="e432d-136">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="e432d-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="e432d-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e432d-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="e432d-138">Detalhes do back-end do cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="e432d-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="e432d-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e432d-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="e432d-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="e432d-141">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="e432d-142">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="e432d-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="e432d-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="e432d-144">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="e432d-145">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="e432d-146">-Título</span><span class="sxs-lookup"><span data-stu-id="e432d-146">-Title</span></span>
<span data-ttu-id="e432d-147">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-147">Backend Title.</span></span>
<span data-ttu-id="e432d-148">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e432d-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="e432d-149">-URL</span><span class="sxs-lookup"><span data-stu-id="e432d-149">-Url</span></span>
<span data-ttu-id="e432d-150">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="e432d-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="e432d-151">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e432d-151">This parameter is required.</span></span>

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

### <span data-ttu-id="e432d-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e432d-152">-Confirm</span></span>
<span data-ttu-id="e432d-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e432d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e432d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e432d-154">-WhatIf</span></span>
<span data-ttu-id="e432d-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e432d-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e432d-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e432d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e432d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e432d-157">CommonParameters</span></span>
<span data-ttu-id="e432d-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e432d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e432d-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e432d-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e432d-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e432d-160">INPUTS</span></span>

### <span data-ttu-id="e432d-161">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e432d-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e432d-162">System. String</span><span class="sxs-lookup"><span data-stu-id="e432d-162">System.String</span></span>

### <span data-ttu-id="e432d-163">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e432d-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e432d-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e432d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="e432d-165">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e432d-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="e432d-166">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e432d-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="e432d-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e432d-167">OUTPUTS</span></span>

### <span data-ttu-id="e432d-168">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e432d-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e432d-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e432d-169">NOTES</span></span>

## <span data-ttu-id="e432d-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e432d-170">RELATED LINKS</span></span>

[<span data-ttu-id="e432d-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e432d-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="e432d-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e432d-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e432d-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e432d-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e432d-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e432d-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e432d-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e432d-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

