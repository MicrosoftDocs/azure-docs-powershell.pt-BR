---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: cd9ce1d65a2adf13f0f33620ba41b75f394011b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405407"
---
# <span data-ttu-id="7fcc5-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fcc5-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="7fcc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fcc5-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcc5-103">Cria uma nova entidade back-end.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="7fcc5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fcc5-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fcc5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fcc5-105">DESCRIPTION</span></span>
<span data-ttu-id="7fcc5-106">Cria uma nova entidade back-end no Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="7fcc5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7fcc5-107">EXAMPLES</span></span>

### <span data-ttu-id="7fcc5-108">Criar Backend 123 com um Esquema de Autorização Básico</span><span class="sxs-lookup"><span data-stu-id="7fcc5-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="7fcc5-109">Cria um novo Backend</span><span class="sxs-lookup"><span data-stu-id="7fcc5-109">Creates a new Backend</span></span>

## <span data-ttu-id="7fcc5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fcc5-110">PARAMETERS</span></span>

### <span data-ttu-id="7fcc5-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="7fcc5-111">-BackendId</span></span>
<span data-ttu-id="7fcc5-112">Identificador de novo back-end.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-112">Identifier of new backend.</span></span>
<span data-ttu-id="7fcc5-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-113">This parameter is optional.</span></span>
<span data-ttu-id="7fcc5-114">Se não especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="7fcc5-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7fcc5-115">-Context</span></span>
<span data-ttu-id="7fcc5-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7fcc5-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-117">This parameter is required.</span></span>

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

### <span data-ttu-id="7fcc5-118">-Credencial</span><span class="sxs-lookup"><span data-stu-id="7fcc5-118">-Credential</span></span>
<span data-ttu-id="7fcc5-119">Detalhes da credencial que devem ser usados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="7fcc5-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="7fcc5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcc5-121">-DefaultProfile</span></span>
<span data-ttu-id="7fcc5-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fcc5-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7fcc5-123">-Description</span></span>
<span data-ttu-id="7fcc5-124">Backend Description.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-124">Backend Description.</span></span>
<span data-ttu-id="7fcc5-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="7fcc5-126">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="7fcc5-126">-Protocol</span></span>
<span data-ttu-id="7fcc5-127">Backend Communication protocol.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-127">Backend Communication protocol.</span></span>
<span data-ttu-id="7fcc5-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-128">This parameter is required.</span></span>
<span data-ttu-id="7fcc5-129">Os valores válidos são "http" e "soap".</span><span class="sxs-lookup"><span data-stu-id="7fcc5-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="7fcc5-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="7fcc5-130">-Proxy</span></span>
<span data-ttu-id="7fcc5-131">Detalhes do Servidor Proxy a serem usados ao enviar solicitação para o Backend.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="7fcc5-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="7fcc5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fcc5-133">-ResourceId</span></span>
<span data-ttu-id="7fcc5-134">Uri de Gerenciamento do Recurso no Sistema Externo.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="7fcc5-135">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-135">This parameter is optional.</span></span>
<span data-ttu-id="7fcc5-136">Essa url pode ser a ID de Arm Resource dos Aplicativos Logic, Aplicativos de Função ou Aplicativos da Api.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="7fcc5-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="7fcc5-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="7fcc5-138">Detalhes do Back-end do Cluster de Malha de Serviço.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="7fcc5-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="7fcc5-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="7fcc5-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="7fcc5-141">Se você quer ignorar a validação da cadeia de certificados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="7fcc5-142">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="7fcc5-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="7fcc5-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="7fcc5-144">Se você quer ignorar a Validação de Nome de Certificado ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="7fcc5-145">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="7fcc5-146">-Título</span><span class="sxs-lookup"><span data-stu-id="7fcc5-146">-Title</span></span>
<span data-ttu-id="7fcc5-147">Backend Title.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-147">Backend Title.</span></span>
<span data-ttu-id="7fcc5-148">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="7fcc5-149">-Url</span><span class="sxs-lookup"><span data-stu-id="7fcc5-149">-Url</span></span>
<span data-ttu-id="7fcc5-150">Url de tempo de execução para o Backend.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="7fcc5-151">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-151">This parameter is required.</span></span>

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

### <span data-ttu-id="7fcc5-152">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7fcc5-152">-Confirm</span></span>
<span data-ttu-id="7fcc5-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fcc5-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fcc5-154">-WhatIf</span></span>
<span data-ttu-id="7fcc5-155">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fcc5-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fcc5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcc5-157">CommonParameters</span></span>
<span data-ttu-id="7fcc5-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcc5-159">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fcc5-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcc5-160">Entradas</span><span class="sxs-lookup"><span data-stu-id="7fcc5-160">INPUTS</span></span>

### <span data-ttu-id="7fcc5-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7fcc5-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7fcc5-162">System.String</span><span class="sxs-lookup"><span data-stu-id="7fcc5-162">System.String</span></span>

### <span data-ttu-id="7fcc5-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7fcc5-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7fcc5-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7fcc5-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="7fcc5-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7fcc5-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="7fcc5-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fcc5-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="7fcc5-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="7fcc5-167">OUTPUTS</span></span>

### <span data-ttu-id="7fcc5-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fcc5-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="7fcc5-169">Notas</span><span class="sxs-lookup"><span data-stu-id="7fcc5-169">NOTES</span></span>

## <span data-ttu-id="7fcc5-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fcc5-170">RELATED LINKS</span></span>

[<span data-ttu-id="7fcc5-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fcc5-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="7fcc5-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7fcc5-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="7fcc5-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7fcc5-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="7fcc5-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fcc5-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="7fcc5-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fcc5-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

