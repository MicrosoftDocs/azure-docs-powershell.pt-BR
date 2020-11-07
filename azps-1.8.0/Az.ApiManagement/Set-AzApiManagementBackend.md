---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771342"
---
# <span data-ttu-id="b733c-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b733c-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="b733c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b733c-102">SYNOPSIS</span></span>
<span data-ttu-id="b733c-103">Atualiza um back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-103">Updates a Backend.</span></span>

## <span data-ttu-id="b733c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b733c-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b733c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b733c-105">DESCRIPTION</span></span>
<span data-ttu-id="b733c-106">Atualiza um back-end existente no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="b733c-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="b733c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b733c-107">EXAMPLES</span></span>

### <span data-ttu-id="b733c-108">Atualiza a descrição do back-end 123</span><span class="sxs-lookup"><span data-stu-id="b733c-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="b733c-109">OS</span><span class="sxs-lookup"><span data-stu-id="b733c-109">PARAMETERS</span></span>

### <span data-ttu-id="b733c-110">-Backid</span><span class="sxs-lookup"><span data-stu-id="b733c-110">-BackendId</span></span>
<span data-ttu-id="b733c-111">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-111">Identifier of new backend.</span></span>
<span data-ttu-id="b733c-112">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b733c-112">This parameter is required.</span></span>

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

### <span data-ttu-id="b733c-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b733c-113">-Context</span></span>
<span data-ttu-id="b733c-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b733c-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b733c-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b733c-115">This parameter is required.</span></span>

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

### <span data-ttu-id="b733c-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="b733c-116">-Credential</span></span>
<span data-ttu-id="b733c-117">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="b733c-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="b733c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b733c-119">-DefaultProfile</span></span>
<span data-ttu-id="b733c-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b733c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b733c-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="b733c-121">-Description</span></span>
<span data-ttu-id="b733c-122">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-122">Backend Description.</span></span>
<span data-ttu-id="b733c-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="b733c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b733c-124">-PassThru</span></span>
<span data-ttu-id="b733c-125">Indica que esse cmdlet retorna o  **PsApiManagementBackend** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b733c-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b733c-126">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="b733c-126">-Protocol</span></span>
<span data-ttu-id="b733c-127">Protocolo de comunicação back-end (http ou SOAP).</span><span class="sxs-lookup"><span data-stu-id="b733c-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="b733c-128">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="b733c-128">This parameter is optional</span></span>

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

### <span data-ttu-id="b733c-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="b733c-129">-Proxy</span></span>
<span data-ttu-id="b733c-130">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="b733c-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="b733c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b733c-132">-ResourceId</span></span>
<span data-ttu-id="b733c-133">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="b733c-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="b733c-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-134">This parameter is optional.</span></span>
<span data-ttu-id="b733c-135">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="b733c-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="b733c-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b733c-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="b733c-137">Detalhes do back-end do cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b733c-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="b733c-138">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="b733c-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="b733c-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="b733c-140">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="b733c-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="b733c-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="b733c-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="b733c-143">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="b733c-144">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="b733c-145">-Título</span><span class="sxs-lookup"><span data-stu-id="b733c-145">-Title</span></span>
<span data-ttu-id="b733c-146">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-146">Backend Title.</span></span>
<span data-ttu-id="b733c-147">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="b733c-148">-URL</span><span class="sxs-lookup"><span data-stu-id="b733c-148">-Url</span></span>
<span data-ttu-id="b733c-149">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="b733c-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="b733c-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b733c-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="b733c-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b733c-151">-Confirm</span></span>
<span data-ttu-id="b733c-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b733c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b733c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b733c-153">-WhatIf</span></span>
<span data-ttu-id="b733c-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b733c-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b733c-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b733c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b733c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b733c-156">CommonParameters</span></span>
<span data-ttu-id="b733c-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b733c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b733c-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b733c-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b733c-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b733c-159">INPUTS</span></span>

### <span data-ttu-id="b733c-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b733c-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b733c-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b733c-161">System.String</span></span>

### <span data-ttu-id="b733c-162">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b733c-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b733c-163">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b733c-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="b733c-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b733c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="b733c-165">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b733c-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="b733c-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b733c-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b733c-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b733c-167">OUTPUTS</span></span>

### <span data-ttu-id="b733c-168">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b733c-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="b733c-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b733c-169">NOTES</span></span>

## <span data-ttu-id="b733c-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b733c-170">RELATED LINKS</span></span>

[<span data-ttu-id="b733c-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b733c-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="b733c-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b733c-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b733c-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b733c-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="b733c-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b733c-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b733c-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b733c-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
