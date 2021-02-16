---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: cb7348e31ca80834836b27c97aa7f68e4207ed24
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404319"
---
# <span data-ttu-id="5aef5-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5aef5-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="5aef5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5aef5-102">SYNOPSIS</span></span>
<span data-ttu-id="5aef5-103">Atualiza um Backend.</span><span class="sxs-lookup"><span data-stu-id="5aef5-103">Updates a Backend.</span></span>

## <span data-ttu-id="5aef5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5aef5-104">SYNTAX</span></span>

### <span data-ttu-id="5aef5-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5aef5-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aef5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5aef5-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aef5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5aef5-107">DESCRIPTION</span></span>
<span data-ttu-id="5aef5-108">Atualiza um back-end existente no Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="5aef5-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="5aef5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5aef5-109">EXAMPLES</span></span>

### <span data-ttu-id="5aef5-110">Atualiza a Descrição do Backend 123</span><span class="sxs-lookup"><span data-stu-id="5aef5-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="5aef5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5aef5-111">PARAMETERS</span></span>

### <span data-ttu-id="5aef5-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="5aef5-112">-BackendId</span></span>
<span data-ttu-id="5aef5-113">Identificador de novo back-end.</span><span class="sxs-lookup"><span data-stu-id="5aef5-113">Identifier of new backend.</span></span>
<span data-ttu-id="5aef5-114">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="5aef5-114">This parameter is required.</span></span>

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

### <span data-ttu-id="5aef5-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5aef5-115">-Context</span></span>
<span data-ttu-id="5aef5-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5aef5-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5aef5-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="5aef5-117">This parameter is required.</span></span>

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

### <span data-ttu-id="5aef5-118">-Credencial</span><span class="sxs-lookup"><span data-stu-id="5aef5-118">-Credential</span></span>
<span data-ttu-id="5aef5-119">Detalhes da credencial que devem ser usados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="5aef5-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="5aef5-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="5aef5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aef5-121">-DefaultProfile</span></span>
<span data-ttu-id="5aef5-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5aef5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aef5-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5aef5-123">-Description</span></span>
<span data-ttu-id="5aef5-124">Backend Description.</span><span class="sxs-lookup"><span data-stu-id="5aef5-124">Backend Description.</span></span>
<span data-ttu-id="5aef5-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="5aef5-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5aef5-126">-InputObject</span></span>
<span data-ttu-id="5aef5-127">Instância de PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="5aef5-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="5aef5-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="5aef5-128">This parameter is required.</span></span>

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

### <span data-ttu-id="5aef5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5aef5-129">-PassThru</span></span>
<span data-ttu-id="5aef5-130">Indica que esse cmdlet retorna  **o PsApiManagementBackend** que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="5aef5-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5aef5-131">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="5aef5-131">-Protocol</span></span>
<span data-ttu-id="5aef5-132">Protocolo back-end Communication (http ou soap).</span><span class="sxs-lookup"><span data-stu-id="5aef5-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="5aef5-133">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="5aef5-133">This parameter is optional</span></span>

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

### <span data-ttu-id="5aef5-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="5aef5-134">-Proxy</span></span>
<span data-ttu-id="5aef5-135">Detalhes do Servidor Proxy a serem usados ao enviar solicitação para o Backend.</span><span class="sxs-lookup"><span data-stu-id="5aef5-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="5aef5-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="5aef5-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5aef5-137">-ResourceId</span></span>
<span data-ttu-id="5aef5-138">Uri de Gerenciamento do Recurso no Sistema Externo.</span><span class="sxs-lookup"><span data-stu-id="5aef5-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="5aef5-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-139">This parameter is optional.</span></span>
<span data-ttu-id="5aef5-140">Essa url pode ser a ID de Arm Resource dos Aplicativos Logic, Aplicativos de Função ou Aplicativos da Api.</span><span class="sxs-lookup"><span data-stu-id="5aef5-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="5aef5-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5aef5-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="5aef5-142">Detalhes do Back-end do Cluster de Malha de Serviço.</span><span class="sxs-lookup"><span data-stu-id="5aef5-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="5aef5-143">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="5aef5-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="5aef5-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="5aef5-145">Se você quer ignorar a validação da cadeia de certificados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="5aef5-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="5aef5-146">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="5aef5-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="5aef5-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="5aef5-148">Se você quer ignorar a Validação de Nome de Certificado ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="5aef5-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="5aef5-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="5aef5-150">-Título</span><span class="sxs-lookup"><span data-stu-id="5aef5-150">-Title</span></span>
<span data-ttu-id="5aef5-151">Backend Title.</span><span class="sxs-lookup"><span data-stu-id="5aef5-151">Backend Title.</span></span>
<span data-ttu-id="5aef5-152">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="5aef5-153">-Url</span><span class="sxs-lookup"><span data-stu-id="5aef5-153">-Url</span></span>
<span data-ttu-id="5aef5-154">Url de tempo de execução para o Backend.</span><span class="sxs-lookup"><span data-stu-id="5aef5-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="5aef5-155">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5aef5-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="5aef5-156">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5aef5-156">-Confirm</span></span>
<span data-ttu-id="5aef5-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aef5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aef5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aef5-158">-WhatIf</span></span>
<span data-ttu-id="5aef5-159">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5aef5-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5aef5-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5aef5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aef5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aef5-161">CommonParameters</span></span>
<span data-ttu-id="5aef5-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aef5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aef5-163">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5aef5-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aef5-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="5aef5-164">INPUTS</span></span>

### <span data-ttu-id="5aef5-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5aef5-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5aef5-166">System.String</span><span class="sxs-lookup"><span data-stu-id="5aef5-166">System.String</span></span>

### <span data-ttu-id="5aef5-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5aef5-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5aef5-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="5aef5-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="5aef5-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="5aef5-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="5aef5-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5aef5-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="5aef5-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5aef5-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5aef5-172">Saídas</span><span class="sxs-lookup"><span data-stu-id="5aef5-172">OUTPUTS</span></span>

### <span data-ttu-id="5aef5-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5aef5-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="5aef5-174">Notas</span><span class="sxs-lookup"><span data-stu-id="5aef5-174">NOTES</span></span>

## <span data-ttu-id="5aef5-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5aef5-175">RELATED LINKS</span></span>

[<span data-ttu-id="5aef5-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5aef5-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="5aef5-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5aef5-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="5aef5-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="5aef5-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="5aef5-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="5aef5-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="5aef5-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5aef5-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
