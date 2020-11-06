---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: f5cf0d9f80b15f178cb701b4474fa5dc13d957eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597944"
---
# <span data-ttu-id="87f07-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="87f07-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="87f07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87f07-102">SYNOPSIS</span></span>
<span data-ttu-id="87f07-103">Atualiza um back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-103">Updates a Backend.</span></span>

## <span data-ttu-id="87f07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87f07-104">SYNTAX</span></span>

### <span data-ttu-id="87f07-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="87f07-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87f07-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="87f07-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87f07-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87f07-107">DESCRIPTION</span></span>
<span data-ttu-id="87f07-108">Atualiza um back-end existente no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="87f07-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="87f07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87f07-109">EXAMPLES</span></span>

### <span data-ttu-id="87f07-110">Atualiza a descrição do back-end 123</span><span class="sxs-lookup"><span data-stu-id="87f07-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="87f07-111">OS</span><span class="sxs-lookup"><span data-stu-id="87f07-111">PARAMETERS</span></span>

### <span data-ttu-id="87f07-112">-Backid</span><span class="sxs-lookup"><span data-stu-id="87f07-112">-BackendId</span></span>
<span data-ttu-id="87f07-113">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-113">Identifier of new backend.</span></span>
<span data-ttu-id="87f07-114">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="87f07-114">This parameter is required.</span></span>

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

### <span data-ttu-id="87f07-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="87f07-115">-Context</span></span>
<span data-ttu-id="87f07-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="87f07-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="87f07-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="87f07-117">This parameter is required.</span></span>

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

### <span data-ttu-id="87f07-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="87f07-118">-Credential</span></span>
<span data-ttu-id="87f07-119">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="87f07-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="87f07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f07-121">-DefaultProfile</span></span>
<span data-ttu-id="87f07-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87f07-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87f07-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="87f07-123">-Description</span></span>
<span data-ttu-id="87f07-124">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-124">Backend Description.</span></span>
<span data-ttu-id="87f07-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="87f07-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87f07-126">-InputObject</span></span>
<span data-ttu-id="87f07-127">Instância do PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="87f07-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="87f07-128">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="87f07-128">This parameter is required.</span></span>

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

### <span data-ttu-id="87f07-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87f07-129">-PassThru</span></span>
<span data-ttu-id="87f07-130">Indica que esse cmdlet retorna o  **PsApiManagementBackend** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="87f07-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87f07-131">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="87f07-131">-Protocol</span></span>
<span data-ttu-id="87f07-132">Protocolo de comunicação back-end (http ou SOAP).</span><span class="sxs-lookup"><span data-stu-id="87f07-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="87f07-133">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="87f07-133">This parameter is optional</span></span>

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

### <span data-ttu-id="87f07-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="87f07-134">-Proxy</span></span>
<span data-ttu-id="87f07-135">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="87f07-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="87f07-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87f07-137">-ResourceId</span></span>
<span data-ttu-id="87f07-138">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="87f07-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="87f07-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-139">This parameter is optional.</span></span>
<span data-ttu-id="87f07-140">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="87f07-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="87f07-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="87f07-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="87f07-142">Detalhes do back-end do cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="87f07-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="87f07-143">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="87f07-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="87f07-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="87f07-145">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="87f07-146">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="87f07-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="87f07-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="87f07-148">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="87f07-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="87f07-150">-Título</span><span class="sxs-lookup"><span data-stu-id="87f07-150">-Title</span></span>
<span data-ttu-id="87f07-151">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-151">Backend Title.</span></span>
<span data-ttu-id="87f07-152">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="87f07-153">-URL</span><span class="sxs-lookup"><span data-stu-id="87f07-153">-Url</span></span>
<span data-ttu-id="87f07-154">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="87f07-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="87f07-155">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f07-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="87f07-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87f07-156">-Confirm</span></span>
<span data-ttu-id="87f07-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87f07-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87f07-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87f07-158">-WhatIf</span></span>
<span data-ttu-id="87f07-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87f07-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87f07-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87f07-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87f07-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f07-161">CommonParameters</span></span>
<span data-ttu-id="87f07-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87f07-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f07-163">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87f07-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f07-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87f07-164">INPUTS</span></span>

### <span data-ttu-id="87f07-165">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87f07-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87f07-166">System. String</span><span class="sxs-lookup"><span data-stu-id="87f07-166">System.String</span></span>

### <span data-ttu-id="87f07-167">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="87f07-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="87f07-168">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="87f07-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="87f07-169">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="87f07-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="87f07-170">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="87f07-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="87f07-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87f07-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87f07-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87f07-172">OUTPUTS</span></span>

### <span data-ttu-id="87f07-173">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="87f07-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="87f07-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87f07-174">NOTES</span></span>

## <span data-ttu-id="87f07-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87f07-175">RELATED LINKS</span></span>

[<span data-ttu-id="87f07-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="87f07-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="87f07-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="87f07-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="87f07-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="87f07-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="87f07-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="87f07-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="87f07-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="87f07-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
