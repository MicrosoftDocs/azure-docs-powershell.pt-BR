---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 2dc2356557a56ced2c0c09b70a1f6c2787438034
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774473"
---
# <span data-ttu-id="de9a3-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de9a3-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="de9a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="de9a3-103">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="de9a3-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="de9a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de9a3-104">SYNTAX</span></span>

### <span data-ttu-id="de9a3-105">Eles</span><span class="sxs-lookup"><span data-stu-id="de9a3-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de9a3-106">S2</span><span class="sxs-lookup"><span data-stu-id="de9a3-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de9a3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de9a3-107">DESCRIPTION</span></span>
<span data-ttu-id="de9a3-108">O cmdlet **set-AzWebApp** define um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="de9a3-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="de9a3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de9a3-109">EXAMPLES</span></span>

### <span data-ttu-id="de9a3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de9a3-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="de9a3-111">Esse comando altera o plano appservice associado ao Slot001, no WebApp ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="de9a3-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="de9a3-112">Use o link para saber mais sobre como alterar o plano appservice e restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="de9a3-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="de9a3-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="de9a3-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="de9a3-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="de9a3-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="de9a3-115">Esse comando define HttpLoggingEnabled como true para o slot Slot001 pertencentes ao ContosoWebApp do aplicativo Web associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="de9a3-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="de9a3-116">OS</span><span class="sxs-lookup"><span data-stu-id="de9a3-116">PARAMETERS</span></span>

### <span data-ttu-id="de9a3-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="de9a3-117">-AppServicePlan</span></span>
<span data-ttu-id="de9a3-118">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="de9a3-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="de9a3-119">-AppSettings</span></span>
<span data-ttu-id="de9a3-120">HashTable das configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de9a3-120">App Settings HashTable.</span></span> <span data-ttu-id="de9a3-121">As configurações do aplicativo existente serão substituídas, removendo as configurações não fornecidas.</span><span class="sxs-lookup"><span data-stu-id="de9a3-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de9a3-122">-AsJob</span></span>
<span data-ttu-id="de9a3-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="de9a3-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="de9a3-124">-AssignIdentity</span></span>
<span data-ttu-id="de9a3-125">Habilitar/desabilitar o MSI em um slot existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="de9a3-125">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="de9a3-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="de9a3-127">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="de9a3-127">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="de9a3-128">-AzureStoragePath</span></span>
<span data-ttu-id="de9a3-129">Armazenamento do Azure para montagem dentro de um aplicativo Web para contêiner.</span><span class="sxs-lookup"><span data-stu-id="de9a3-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="de9a3-130">Usar o New-AzureRmWebAppAzureStoragePath para criá-lo</span><span class="sxs-lookup"><span data-stu-id="de9a3-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="de9a3-131">-ConnectionStrings</span></span>
<span data-ttu-id="de9a3-132">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="de9a3-132">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="de9a3-133">-ContainerImageName</span></span>
<span data-ttu-id="de9a3-134">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="de9a3-134">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="de9a3-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="de9a3-136">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="de9a3-136">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="de9a3-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="de9a3-138">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="de9a3-138">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="de9a3-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="de9a3-140">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="de9a3-140">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-141">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="de9a3-141">-DefaultDocuments</span></span>
<span data-ttu-id="de9a3-142">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="de9a3-142">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de9a3-143">-DefaultProfile</span></span>
<span data-ttu-id="de9a3-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de9a3-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de9a3-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="de9a3-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="de9a3-146">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="de9a3-146">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="de9a3-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="de9a3-148">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="de9a3-148">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="de9a3-149">-HandlerMappings</span></span>
<span data-ttu-id="de9a3-150">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="de9a3-150">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="de9a3-151">-HttpLoggingEnabled</span></span>
<span data-ttu-id="de9a3-152">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="de9a3-152">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="de9a3-153">-HttpsOnly</span></span>
<span data-ttu-id="de9a3-154">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um slot existente</span><span class="sxs-lookup"><span data-stu-id="de9a3-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="de9a3-155">-ManagedPipelineMode</span></span>
<span data-ttu-id="de9a3-156">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="de9a3-156">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="de9a3-157">-Name</span></span>
<span data-ttu-id="de9a3-158">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="de9a3-158">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="de9a3-159">-NetFrameworkVersion</span></span>
<span data-ttu-id="de9a3-160">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="de9a3-160">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="de9a3-161">-NumberOfWorkers</span></span>
<span data-ttu-id="de9a3-162">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="de9a3-162">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="de9a3-163">-PhpVersion</span></span>
<span data-ttu-id="de9a3-164">Versão do php</span><span class="sxs-lookup"><span data-stu-id="de9a3-164">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="de9a3-165">-RequestTracingEnabled</span></span>
<span data-ttu-id="de9a3-166">Booleano de rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="de9a3-166">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de9a3-167">-ResourceGroupName</span></span>
<span data-ttu-id="de9a3-168">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="de9a3-168">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-169">-Slot</span><span class="sxs-lookup"><span data-stu-id="de9a3-169">-Slot</span></span>
<span data-ttu-id="de9a3-170">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="de9a3-170">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="de9a3-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="de9a3-172">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="de9a3-172">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="de9a3-173">-WebApp</span></span>
<span data-ttu-id="de9a3-174">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="de9a3-174">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="de9a3-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="de9a3-176">Booleano habilitados para Web Sockets</span><span class="sxs-lookup"><span data-stu-id="de9a3-176">Web Sockets Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a3-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9a3-177">CommonParameters</span></span>
<span data-ttu-id="de9a3-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de9a3-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9a3-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de9a3-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9a3-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de9a3-180">INPUTS</span></span>

### <span data-ttu-id="de9a3-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="de9a3-181">System.Int32</span></span>

### <span data-ttu-id="de9a3-182">System. String</span><span class="sxs-lookup"><span data-stu-id="de9a3-182">System.String</span></span>

### <span data-ttu-id="de9a3-183">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="de9a3-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de9a3-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de9a3-184">OUTPUTS</span></span>

### <span data-ttu-id="de9a3-185">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="de9a3-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de9a3-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de9a3-186">NOTES</span></span>

## <span data-ttu-id="de9a3-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de9a3-187">RELATED LINKS</span></span>

[<span data-ttu-id="de9a3-188">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de9a3-188">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="de9a3-189">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de9a3-189">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="de9a3-190">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de9a3-190">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="de9a3-191">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de9a3-191">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="de9a3-192">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de9a3-192">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="de9a3-193">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de9a3-193">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="de9a3-194">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="de9a3-194">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
