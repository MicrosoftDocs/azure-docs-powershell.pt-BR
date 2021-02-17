---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 8631120178a256aa1ec5b817727f9362f6d8f076
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407277"
---
# <span data-ttu-id="89b5a-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89b5a-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="89b5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="89b5a-103">Atualiza um Backend.</span><span class="sxs-lookup"><span data-stu-id="89b5a-103">Updates a Backend.</span></span>

## <span data-ttu-id="89b5a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89b5a-104">SYNTAX</span></span>

### <span data-ttu-id="89b5a-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="89b5a-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89b5a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="89b5a-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89b5a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="89b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="89b5a-108">Atualiza um back-end existente no Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="89b5a-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="89b5a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89b5a-109">EXAMPLES</span></span>

### <span data-ttu-id="89b5a-110">Atualiza a Descrição do Backend 123</span><span class="sxs-lookup"><span data-stu-id="89b5a-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="89b5a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89b5a-111">PARAMETERS</span></span>

### <span data-ttu-id="89b5a-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="89b5a-112">-BackendId</span></span>
<span data-ttu-id="89b5a-113">Identificador de novo back-end.</span><span class="sxs-lookup"><span data-stu-id="89b5a-113">Identifier of new backend.</span></span>
<span data-ttu-id="89b5a-114">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="89b5a-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b5a-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="89b5a-115">-Context</span></span>
<span data-ttu-id="89b5a-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="89b5a-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="89b5a-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="89b5a-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89b5a-118">-Credencial</span><span class="sxs-lookup"><span data-stu-id="89b5a-118">-Credential</span></span>
<span data-ttu-id="89b5a-119">Detalhes da credencial que devem ser usados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="89b5a-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="89b5a-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="89b5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b5a-121">-DefaultProfile</span></span>
<span data-ttu-id="89b5a-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="89b5a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89b5a-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="89b5a-123">-Description</span></span>
<span data-ttu-id="89b5a-124">Backend Description.</span><span class="sxs-lookup"><span data-stu-id="89b5a-124">Backend Description.</span></span>
<span data-ttu-id="89b5a-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="89b5a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89b5a-126">-InputObject</span></span>
<span data-ttu-id="89b5a-127">Instância de PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="89b5a-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="89b5a-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="89b5a-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89b5a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89b5a-129">-PassThru</span></span>
<span data-ttu-id="89b5a-130">Indica que esse cmdlet retorna  **o PsApiManagementBackend** que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="89b5a-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b5a-131">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="89b5a-131">-Protocol</span></span>
<span data-ttu-id="89b5a-132">Protocolo back-end Communication (http ou soap).</span><span class="sxs-lookup"><span data-stu-id="89b5a-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="89b5a-133">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="89b5a-133">This parameter is optional</span></span>

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

### <span data-ttu-id="89b5a-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="89b5a-134">-Proxy</span></span>
<span data-ttu-id="89b5a-135">Detalhes do Servidor Proxy a serem usados ao enviar solicitação para o Backend.</span><span class="sxs-lookup"><span data-stu-id="89b5a-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="89b5a-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="89b5a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89b5a-137">-ResourceId</span></span>
<span data-ttu-id="89b5a-138">Uri de Gerenciamento do Recurso no Sistema Externo.</span><span class="sxs-lookup"><span data-stu-id="89b5a-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="89b5a-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-139">This parameter is optional.</span></span>
<span data-ttu-id="89b5a-140">Essa url pode ser a ID de Arm Resource dos Aplicativos Logic, Aplicativos de Função ou Aplicativos da Api.</span><span class="sxs-lookup"><span data-stu-id="89b5a-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="89b5a-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="89b5a-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="89b5a-142">Detalhes do Back-end do Cluster de Malha de Serviço.</span><span class="sxs-lookup"><span data-stu-id="89b5a-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="89b5a-143">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="89b5a-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="89b5a-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="89b5a-145">Se você quer ignorar a validação da cadeia de certificados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="89b5a-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="89b5a-146">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="89b5a-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="89b5a-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="89b5a-148">Se você quer ignorar a Validação de Nome de Certificado ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="89b5a-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="89b5a-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="89b5a-150">-Título</span><span class="sxs-lookup"><span data-stu-id="89b5a-150">-Title</span></span>
<span data-ttu-id="89b5a-151">Backend Title.</span><span class="sxs-lookup"><span data-stu-id="89b5a-151">Backend Title.</span></span>
<span data-ttu-id="89b5a-152">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="89b5a-153">-Url</span><span class="sxs-lookup"><span data-stu-id="89b5a-153">-Url</span></span>
<span data-ttu-id="89b5a-154">Url de tempo de execução para o Backend.</span><span class="sxs-lookup"><span data-stu-id="89b5a-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="89b5a-155">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89b5a-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="89b5a-156">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="89b5a-156">-Confirm</span></span>
<span data-ttu-id="89b5a-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89b5a-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89b5a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89b5a-158">-WhatIf</span></span>
<span data-ttu-id="89b5a-159">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="89b5a-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89b5a-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89b5a-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89b5a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b5a-161">CommonParameters</span></span>
<span data-ttu-id="89b5a-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b5a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b5a-163">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89b5a-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b5a-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="89b5a-164">INPUTS</span></span>

### <span data-ttu-id="89b5a-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="89b5a-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="89b5a-166">System.String</span><span class="sxs-lookup"><span data-stu-id="89b5a-166">System.String</span></span>

### <span data-ttu-id="89b5a-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="89b5a-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="89b5a-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="89b5a-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="89b5a-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="89b5a-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="89b5a-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="89b5a-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="89b5a-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89b5a-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89b5a-172">Saídas</span><span class="sxs-lookup"><span data-stu-id="89b5a-172">OUTPUTS</span></span>

### <span data-ttu-id="89b5a-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89b5a-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="89b5a-174">Notas</span><span class="sxs-lookup"><span data-stu-id="89b5a-174">NOTES</span></span>

## <span data-ttu-id="89b5a-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89b5a-175">RELATED LINKS</span></span>

[<span data-ttu-id="89b5a-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89b5a-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="89b5a-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89b5a-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="89b5a-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="89b5a-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="89b5a-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="89b5a-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="89b5a-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89b5a-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
