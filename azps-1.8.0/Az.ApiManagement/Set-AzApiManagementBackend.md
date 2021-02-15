---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 0ac89ed099029fbbabe90e07da7ba9c204449db9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400732"
---
# <span data-ttu-id="8e5a7-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8e5a7-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="8e5a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5a7-103">Atualiza um Backend.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-103">Updates a Backend.</span></span>

## <span data-ttu-id="8e5a7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e5a7-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e5a7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="8e5a7-106">Atualiza um back-end existente no Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="8e5a7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="8e5a7-108">Atualiza a Descrição do Backend 123</span><span class="sxs-lookup"><span data-stu-id="8e5a7-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="8e5a7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e5a7-109">PARAMETERS</span></span>

### <span data-ttu-id="8e5a7-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="8e5a7-110">-BackendId</span></span>
<span data-ttu-id="8e5a7-111">Identificador de novo back-end.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-111">Identifier of new backend.</span></span>
<span data-ttu-id="8e5a7-112">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-112">This parameter is required.</span></span>

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

### <span data-ttu-id="8e5a7-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8e5a7-113">-Context</span></span>
<span data-ttu-id="8e5a7-114">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8e5a7-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-115">This parameter is required.</span></span>

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

### <span data-ttu-id="8e5a7-116">-Credencial</span><span class="sxs-lookup"><span data-stu-id="8e5a7-116">-Credential</span></span>
<span data-ttu-id="8e5a7-117">Detalhes da credencial que devem ser usados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="8e5a7-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e5a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5a7-119">-DefaultProfile</span></span>
<span data-ttu-id="8e5a7-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e5a7-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8e5a7-121">-Description</span></span>
<span data-ttu-id="8e5a7-122">Backend Description.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-122">Backend Description.</span></span>
<span data-ttu-id="8e5a7-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e5a7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e5a7-124">-PassThru</span></span>
<span data-ttu-id="8e5a7-125">Indica que esse cmdlet retorna  **o PsApiManagementBackend** que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8e5a7-126">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="8e5a7-126">-Protocol</span></span>
<span data-ttu-id="8e5a7-127">Protocolo back-end Communication (http ou soap).</span><span class="sxs-lookup"><span data-stu-id="8e5a7-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="8e5a7-128">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="8e5a7-128">This parameter is optional</span></span>

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

### <span data-ttu-id="8e5a7-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="8e5a7-129">-Proxy</span></span>
<span data-ttu-id="8e5a7-130">Detalhes do Servidor Proxy a serem usados ao enviar solicitação para o Backend.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="8e5a7-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e5a7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e5a7-132">-ResourceId</span></span>
<span data-ttu-id="8e5a7-133">Uri de Gerenciamento do Recurso no Sistema Externo.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="8e5a7-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-134">This parameter is optional.</span></span>
<span data-ttu-id="8e5a7-135">Essa url pode ser a ID de Arm Resource dos Aplicativos Logic, Aplicativos de Função ou Aplicativos da Api.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="8e5a7-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="8e5a7-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="8e5a7-137">Detalhes do Back-end do Cluster de Malha de Serviço.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="8e5a7-138">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e5a7-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="8e5a7-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="8e5a7-140">Se você quer ignorar a validação da cadeia de certificados ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="8e5a7-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e5a7-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="8e5a7-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="8e5a7-143">Se você quer ignorar a Validação de Nome de Certificado ao falar com o Backend.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="8e5a7-144">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e5a7-145">-Título</span><span class="sxs-lookup"><span data-stu-id="8e5a7-145">-Title</span></span>
<span data-ttu-id="8e5a7-146">Backend Title.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-146">Backend Title.</span></span>
<span data-ttu-id="8e5a7-147">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e5a7-148">-Url</span><span class="sxs-lookup"><span data-stu-id="8e5a7-148">-Url</span></span>
<span data-ttu-id="8e5a7-149">Url de tempo de execução para o Backend.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="8e5a7-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e5a7-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8e5a7-151">-Confirm</span></span>
<span data-ttu-id="8e5a7-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e5a7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e5a7-153">-WhatIf</span></span>
<span data-ttu-id="8e5a7-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e5a7-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e5a7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5a7-156">CommonParameters</span></span>
<span data-ttu-id="8e5a7-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5a7-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5a7-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5a7-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e5a7-159">INPUTS</span></span>

### <span data-ttu-id="8e5a7-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8e5a7-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8e5a7-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8e5a7-161">System.String</span></span>

### <span data-ttu-id="8e5a7-162">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e5a7-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8e5a7-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8e5a7-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="8e5a7-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8e5a7-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="8e5a7-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e5a7-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="8e5a7-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8e5a7-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8e5a7-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e5a7-167">OUTPUTS</span></span>

### <span data-ttu-id="8e5a7-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8e5a7-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="8e5a7-169">Notas</span><span class="sxs-lookup"><span data-stu-id="8e5a7-169">NOTES</span></span>

## <span data-ttu-id="8e5a7-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e5a7-170">RELATED LINKS</span></span>

[<span data-ttu-id="8e5a7-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8e5a7-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="8e5a7-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8e5a7-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="8e5a7-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8e5a7-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="8e5a7-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8e5a7-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="8e5a7-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8e5a7-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
