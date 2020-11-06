---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 52e159ae0f9d1b94b316394ddefe04f0bd8aa1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426487"
---
# <span data-ttu-id="d1ca3-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d1ca3-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d1ca3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ca3-103">Atualiza um back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1ca3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1ca3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1ca3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="d1ca3-106">Atualiza um back-end existente no gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="d1ca3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="d1ca3-108">Atualiza a descrição do back-end 123</span><span class="sxs-lookup"><span data-stu-id="d1ca3-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="d1ca3-109">OS</span><span class="sxs-lookup"><span data-stu-id="d1ca3-109">PARAMETERS</span></span>

### <span data-ttu-id="d1ca3-110">-Backid</span><span class="sxs-lookup"><span data-stu-id="d1ca3-110">-BackendId</span></span>
<span data-ttu-id="d1ca3-111">Identificador do novo back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-111">Identifier of new backend.</span></span>
<span data-ttu-id="d1ca3-112">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-112">This parameter is required.</span></span>

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

### <span data-ttu-id="d1ca3-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d1ca3-113">-Context</span></span>
<span data-ttu-id="d1ca3-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d1ca3-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d1ca3-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="d1ca3-116">-Credential</span></span>
<span data-ttu-id="d1ca3-117">Detalhes da credencial que devem ser usados ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="d1ca3-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1ca3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ca3-119">-DefaultProfile</span></span>
<span data-ttu-id="d1ca3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca3-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d1ca3-121">-Description</span></span>
<span data-ttu-id="d1ca3-122">Descrição de back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-122">Backend Description.</span></span>
<span data-ttu-id="d1ca3-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1ca3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1ca3-124">-PassThru</span></span>
<span data-ttu-id="d1ca3-125">Indica que esse cmdlet retorna o  **PsApiManagementBackend** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d1ca3-126">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="d1ca3-126">-Protocol</span></span>
<span data-ttu-id="d1ca3-127">Protocolo de comunicação back-end (http ou SOAP).</span><span class="sxs-lookup"><span data-stu-id="d1ca3-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="d1ca3-128">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="d1ca3-128">This parameter is optional</span></span>

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

### <span data-ttu-id="d1ca3-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="d1ca3-129">-Proxy</span></span>
<span data-ttu-id="d1ca3-130">Detalhes do servidor proxy a serem usados ao enviar solicitação ao back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="d1ca3-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1ca3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1ca3-132">-ResourceId</span></span>
<span data-ttu-id="d1ca3-133">URI de gerenciamento do recurso em sistema externo.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="d1ca3-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-134">This parameter is optional.</span></span>
<span data-ttu-id="d1ca3-135">Essa URL pode ser a ID do recurso ARM de aplicativos lógicos, aplicativos de função ou aplicativos de API.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="d1ca3-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d1ca3-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="d1ca3-137">Detalhes do back-end do cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="d1ca3-138">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1ca3-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="d1ca3-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="d1ca3-140">Se deseja ignorar a validação da cadeia de certificados ao conversar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="d1ca3-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1ca3-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="d1ca3-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="d1ca3-143">Se deve ser ignorada a validação do nome do certificado ao se comunicar com o back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="d1ca3-144">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1ca3-145">-Título</span><span class="sxs-lookup"><span data-stu-id="d1ca3-145">-Title</span></span>
<span data-ttu-id="d1ca3-146">Título de back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-146">Backend Title.</span></span>
<span data-ttu-id="d1ca3-147">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1ca3-148">-URL</span><span class="sxs-lookup"><span data-stu-id="d1ca3-148">-Url</span></span>
<span data-ttu-id="d1ca3-149">URL do tempo de execução para o back-end.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="d1ca3-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1ca3-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1ca3-151">-Confirm</span></span>
<span data-ttu-id="d1ca3-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1ca3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ca3-153">-WhatIf</span></span>
<span data-ttu-id="d1ca3-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1ca3-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1ca3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ca3-156">CommonParameters</span></span>
<span data-ttu-id="d1ca3-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ca3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ca3-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ca3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ca3-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1ca3-159">INPUTS</span></span>

### <span data-ttu-id="d1ca3-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1ca3-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1ca3-161">System. String</span><span class="sxs-lookup"><span data-stu-id="d1ca3-161">System.String</span></span>

### <span data-ttu-id="d1ca3-162">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d1ca3-162">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d1ca3-163">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d1ca3-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="d1ca3-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d1ca3-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="d1ca3-165">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1ca3-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="d1ca3-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1ca3-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1ca3-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1ca3-167">OUTPUTS</span></span>

### <span data-ttu-id="d1ca3-168">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d1ca3-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d1ca3-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1ca3-169">NOTES</span></span>

## <span data-ttu-id="d1ca3-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1ca3-170">RELATED LINKS</span></span>

[<span data-ttu-id="d1ca3-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d1ca3-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d1ca3-172">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d1ca3-172">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d1ca3-173">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d1ca3-173">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d1ca3-174">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d1ca3-174">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d1ca3-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d1ca3-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
