---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 30947e52e5a7afaa8bf2890b95f48f6bb6f36bce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943859"
---
# <span data-ttu-id="a0e8e-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0e8e-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="a0e8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e8e-103">Atualiza um back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-103">Updates a Backend.</span></span>

## <span data-ttu-id="a0e8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0e8e-104">SYNTAX</span></span>

### <span data-ttu-id="a0e8e-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0e8e-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0e8e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0e8e-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0e8e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0e8e-107">DESCRIPTION</span></span>
<span data-ttu-id="a0e8e-108">Atualiza um back-end existente no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="a0e8e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0e8e-109">EXAMPLES</span></span>

### <span data-ttu-id="a0e8e-110">Atualiza a descrição do back-end 123</span><span class="sxs-lookup"><span data-stu-id="a0e8e-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="a0e8e-111">OS</span><span class="sxs-lookup"><span data-stu-id="a0e8e-111">PARAMETERS</span></span>

### <span data-ttu-id="a0e8e-112">-Backid</span><span class="sxs-lookup"><span data-stu-id="a0e8e-112">-BackendId</span></span>
<span data-ttu-id="a0e8e-113">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-113">Identifier of new backend.</span></span>
<span data-ttu-id="a0e8e-114">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-114">This parameter is required.</span></span>

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

### <span data-ttu-id="a0e8e-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a0e8e-115">-Context</span></span>
<span data-ttu-id="a0e8e-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a0e8e-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-117">This parameter is required.</span></span>

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

### <span data-ttu-id="a0e8e-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="a0e8e-118">-Credential</span></span>
<span data-ttu-id="a0e8e-119">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="a0e8e-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0e8e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e8e-121">-DefaultProfile</span></span>
<span data-ttu-id="a0e8e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0e8e-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a0e8e-123">-Description</span></span>
<span data-ttu-id="a0e8e-124">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-124">Backend Description.</span></span>
<span data-ttu-id="a0e8e-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0e8e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0e8e-126">-InputObject</span></span>
<span data-ttu-id="a0e8e-127">Instância do PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="a0e8e-128">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-128">This parameter is required.</span></span>

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

### <span data-ttu-id="a0e8e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0e8e-129">-PassThru</span></span>
<span data-ttu-id="a0e8e-130">Indica que esse cmdlet retorna o  **PsApiManagementBackend** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a0e8e-131">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="a0e8e-131">-Protocol</span></span>
<span data-ttu-id="a0e8e-132">Protocolo de comunicação back-end (http ou SOAP).</span><span class="sxs-lookup"><span data-stu-id="a0e8e-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="a0e8e-133">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="a0e8e-133">This parameter is optional</span></span>

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

### <span data-ttu-id="a0e8e-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="a0e8e-134">-Proxy</span></span>
<span data-ttu-id="a0e8e-135">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="a0e8e-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0e8e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0e8e-137">-ResourceId</span></span>
<span data-ttu-id="a0e8e-138">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="a0e8e-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-139">This parameter is optional.</span></span>
<span data-ttu-id="a0e8e-140">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="a0e8e-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a0e8e-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="a0e8e-142">Detalhes do back-end do cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="a0e8e-143">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0e8e-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="a0e8e-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="a0e8e-145">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="a0e8e-146">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0e8e-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="a0e8e-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="a0e8e-148">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="a0e8e-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0e8e-150">-Título</span><span class="sxs-lookup"><span data-stu-id="a0e8e-150">-Title</span></span>
<span data-ttu-id="a0e8e-151">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-151">Backend Title.</span></span>
<span data-ttu-id="a0e8e-152">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0e8e-153">-URL</span><span class="sxs-lookup"><span data-stu-id="a0e8e-153">-Url</span></span>
<span data-ttu-id="a0e8e-154">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="a0e8e-155">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="a0e8e-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0e8e-156">-Confirm</span></span>
<span data-ttu-id="a0e8e-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e8e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e8e-158">-WhatIf</span></span>
<span data-ttu-id="a0e8e-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0e8e-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e8e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e8e-161">CommonParameters</span></span>
<span data-ttu-id="a0e8e-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e8e-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0e8e-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e8e-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0e8e-164">INPUTS</span></span>

### <span data-ttu-id="a0e8e-165">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a0e8e-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0e8e-166">System. String</span><span class="sxs-lookup"><span data-stu-id="a0e8e-166">System.String</span></span>

### <span data-ttu-id="a0e8e-167">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a0e8e-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a0e8e-168">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a0e8e-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="a0e8e-169">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a0e8e-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="a0e8e-170">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a0e8e-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="a0e8e-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0e8e-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a0e8e-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0e8e-172">OUTPUTS</span></span>

### <span data-ttu-id="a0e8e-173">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0e8e-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="a0e8e-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0e8e-174">NOTES</span></span>

## <span data-ttu-id="a0e8e-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0e8e-175">RELATED LINKS</span></span>

[<span data-ttu-id="a0e8e-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0e8e-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="a0e8e-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0e8e-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="a0e8e-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a0e8e-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="a0e8e-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a0e8e-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="a0e8e-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0e8e-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
