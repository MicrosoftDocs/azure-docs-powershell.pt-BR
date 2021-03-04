---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: ba528724bebfc6ce3400ead69a223e08f42663ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893020"
---
# <span data-ttu-id="362a3-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="362a3-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="362a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="362a3-102">SYNOPSIS</span></span>
<span data-ttu-id="362a3-103">Cria uma nova entidade back-end.</span><span class="sxs-lookup"><span data-stu-id="362a3-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="362a3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="362a3-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="362a3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="362a3-105">DESCRIPTION</span></span>
<span data-ttu-id="362a3-106">Cria uma nova entidade back-end no Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="362a3-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="362a3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="362a3-107">EXAMPLES</span></span>

### <span data-ttu-id="362a3-108">Exemplo 1: Criar Back-end 123 com um Esquema de Autorização Básico</span><span class="sxs-lookup"><span data-stu-id="362a3-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="362a3-109">Cria um novo Backend</span><span class="sxs-lookup"><span data-stu-id="362a3-109">Creates a new Backend</span></span>

## <span data-ttu-id="362a3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="362a3-110">PARAMETERS</span></span>

### <span data-ttu-id="362a3-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="362a3-111">-BackendId</span></span>
<span data-ttu-id="362a3-112">Identificador de novo back-end.</span><span class="sxs-lookup"><span data-stu-id="362a3-112">Identifier of new backend.</span></span>
<span data-ttu-id="362a3-113">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-113">This parameter is optional.</span></span>
<span data-ttu-id="362a3-114">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="362a3-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="362a3-115">-Context</span><span class="sxs-lookup"><span data-stu-id="362a3-115">-Context</span></span>
<span data-ttu-id="362a3-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="362a3-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="362a3-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="362a3-117">This parameter is required.</span></span>

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

### <span data-ttu-id="362a3-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="362a3-118">-Credential</span></span>
<span data-ttu-id="362a3-119">Detalhes da credencial que devem ser usados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="362a3-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="362a3-120">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="362a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362a3-121">-DefaultProfile</span></span>
<span data-ttu-id="362a3-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="362a3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="362a3-123">-Description</span><span class="sxs-lookup"><span data-stu-id="362a3-123">-Description</span></span>
<span data-ttu-id="362a3-124">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="362a3-124">Backend Description.</span></span>
<span data-ttu-id="362a3-125">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="362a3-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="362a3-126">-Protocol</span></span>
<span data-ttu-id="362a3-127">Protocolo de Comunicação back-end.</span><span class="sxs-lookup"><span data-stu-id="362a3-127">Backend Communication protocol.</span></span>
<span data-ttu-id="362a3-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="362a3-128">This parameter is required.</span></span>
<span data-ttu-id="362a3-129">Os valores válidos são 'http' e 'soap'.</span><span class="sxs-lookup"><span data-stu-id="362a3-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="362a3-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="362a3-130">-Proxy</span></span>
<span data-ttu-id="362a3-131">Detalhes do Servidor Proxy a serem usados durante o envio da solicitação para o Backend.</span><span class="sxs-lookup"><span data-stu-id="362a3-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="362a3-132">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="362a3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="362a3-133">-ResourceId</span></span>
<span data-ttu-id="362a3-134">Uri de gerenciamento do Recurso no Sistema Externo.</span><span class="sxs-lookup"><span data-stu-id="362a3-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="362a3-135">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-135">This parameter is optional.</span></span>
<span data-ttu-id="362a3-136">Essa url pode ser a ID de Recurso arm de Aplicativos Lógicos, Aplicativos de Função ou Aplicativos de Api.</span><span class="sxs-lookup"><span data-stu-id="362a3-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="362a3-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="362a3-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="362a3-138">Detalhes do Back-end do Cluster de Malha de Serviço.</span><span class="sxs-lookup"><span data-stu-id="362a3-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="362a3-139">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="362a3-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="362a3-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="362a3-141">Se ignorar a validação da cadeia de certificados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="362a3-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="362a3-142">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="362a3-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="362a3-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="362a3-144">Se deve ignorar Validação de Nome de Certificado ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="362a3-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="362a3-145">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="362a3-146">-Title</span><span class="sxs-lookup"><span data-stu-id="362a3-146">-Title</span></span>
<span data-ttu-id="362a3-147">Título back-end.</span><span class="sxs-lookup"><span data-stu-id="362a3-147">Backend Title.</span></span>
<span data-ttu-id="362a3-148">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="362a3-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="362a3-149">-Url</span><span class="sxs-lookup"><span data-stu-id="362a3-149">-Url</span></span>
<span data-ttu-id="362a3-150">Url do tempo de execução para o Backend.</span><span class="sxs-lookup"><span data-stu-id="362a3-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="362a3-151">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="362a3-151">This parameter is required.</span></span>

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

### <span data-ttu-id="362a3-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="362a3-152">-Confirm</span></span>
<span data-ttu-id="362a3-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="362a3-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="362a3-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="362a3-154">-WhatIf</span></span>
<span data-ttu-id="362a3-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="362a3-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="362a3-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="362a3-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="362a3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362a3-157">CommonParameters</span></span>
<span data-ttu-id="362a3-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362a3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362a3-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="362a3-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362a3-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="362a3-160">INPUTS</span></span>

### <span data-ttu-id="362a3-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="362a3-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="362a3-162">System.String</span><span class="sxs-lookup"><span data-stu-id="362a3-162">System.String</span></span>

### <span data-ttu-id="362a3-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="362a3-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="362a3-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="362a3-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="362a3-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="362a3-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="362a3-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="362a3-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="362a3-167">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="362a3-167">OUTPUTS</span></span>

### <span data-ttu-id="362a3-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="362a3-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="362a3-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="362a3-169">NOTES</span></span>

## <span data-ttu-id="362a3-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="362a3-170">RELATED LINKS</span></span>

[<span data-ttu-id="362a3-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="362a3-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="362a3-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="362a3-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="362a3-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="362a3-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="362a3-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="362a3-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="362a3-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="362a3-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

