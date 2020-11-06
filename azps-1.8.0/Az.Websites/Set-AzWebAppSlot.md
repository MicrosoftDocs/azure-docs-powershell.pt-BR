---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598293"
---
# <span data-ttu-id="bff7d-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bff7d-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="bff7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bff7d-102">SYNOPSIS</span></span>
<span data-ttu-id="bff7d-103">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bff7d-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="bff7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bff7d-104">SYNTAX</span></span>

### <span data-ttu-id="bff7d-105">Eles</span><span class="sxs-lookup"><span data-stu-id="bff7d-105">S1</span></span>
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

### <span data-ttu-id="bff7d-106">S2</span><span class="sxs-lookup"><span data-stu-id="bff7d-106">S2</span></span>
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

## <span data-ttu-id="bff7d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bff7d-107">DESCRIPTION</span></span>
<span data-ttu-id="bff7d-108">O cmdlet **set-AzWebApp** define um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bff7d-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="bff7d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bff7d-109">EXAMPLES</span></span>

### <span data-ttu-id="bff7d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bff7d-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="bff7d-111">Esse comando altera o plano appservice associado ao Slot001, no WebApp ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="bff7d-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="bff7d-112">Use o link para limpar e saber mais sobre como alterar o plano appservice e restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="bff7d-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="bff7d-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="bff7d-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="bff7d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bff7d-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="bff7d-115">Esse comando define HttpLoggingEnabled como true para o slot Slot001 pertencentes ao ContosoWebApp do aplicativo Web associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="bff7d-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="bff7d-116">OS</span><span class="sxs-lookup"><span data-stu-id="bff7d-116">PARAMETERS</span></span>

### <span data-ttu-id="bff7d-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bff7d-117">-AppServicePlan</span></span>
<span data-ttu-id="bff7d-118">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="bff7d-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="bff7d-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="bff7d-119">-AppSettings</span></span>
<span data-ttu-id="bff7d-120">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="bff7d-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="bff7d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bff7d-121">-AsJob</span></span>
<span data-ttu-id="bff7d-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bff7d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bff7d-123">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bff7d-123">-AssignIdentity</span></span>
<span data-ttu-id="bff7d-124">Habilitar/desabilitar o MSI em um slot existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="bff7d-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="bff7d-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="bff7d-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="bff7d-126">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="bff7d-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="bff7d-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="bff7d-127">-AzureStoragePath</span></span>
<span data-ttu-id="bff7d-128">Armazenamento do Azure para montagem dentro de um aplicativo Web para contêiner.</span><span class="sxs-lookup"><span data-stu-id="bff7d-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="bff7d-129">Usar o New-AzureRmWebAppAzureStoragePath para criá-lo</span><span class="sxs-lookup"><span data-stu-id="bff7d-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="bff7d-130">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="bff7d-130">-ConnectionStrings</span></span>
<span data-ttu-id="bff7d-131">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="bff7d-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="bff7d-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="bff7d-132">-ContainerImageName</span></span>
<span data-ttu-id="bff7d-133">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="bff7d-133">Container Image Name</span></span>

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

### <span data-ttu-id="bff7d-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="bff7d-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="bff7d-135">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="bff7d-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="bff7d-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="bff7d-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="bff7d-137">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="bff7d-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="bff7d-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="bff7d-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="bff7d-139">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="bff7d-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="bff7d-140">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="bff7d-140">-DefaultDocuments</span></span>
<span data-ttu-id="bff7d-141">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="bff7d-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="bff7d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff7d-142">-DefaultProfile</span></span>
<span data-ttu-id="bff7d-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bff7d-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff7d-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="bff7d-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="bff7d-145">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="bff7d-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="bff7d-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="bff7d-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="bff7d-147">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="bff7d-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="bff7d-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="bff7d-148">-HandlerMappings</span></span>
<span data-ttu-id="bff7d-149">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="bff7d-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="bff7d-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="bff7d-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="bff7d-151">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="bff7d-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="bff7d-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="bff7d-152">-HttpsOnly</span></span>
<span data-ttu-id="bff7d-153">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um slot existente</span><span class="sxs-lookup"><span data-stu-id="bff7d-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="bff7d-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="bff7d-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="bff7d-155">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="bff7d-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="bff7d-156">-Nome</span><span class="sxs-lookup"><span data-stu-id="bff7d-156">-Name</span></span>
<span data-ttu-id="bff7d-157">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="bff7d-157">WebApp Name</span></span>

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

### <span data-ttu-id="bff7d-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="bff7d-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="bff7d-159">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="bff7d-159">Net Framework Version</span></span>

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

### <span data-ttu-id="bff7d-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="bff7d-160">-NumberOfWorkers</span></span>
<span data-ttu-id="bff7d-161">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="bff7d-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="bff7d-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="bff7d-162">-PhpVersion</span></span>
<span data-ttu-id="bff7d-163">Versão do php</span><span class="sxs-lookup"><span data-stu-id="bff7d-163">Php Version</span></span>

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

### <span data-ttu-id="bff7d-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="bff7d-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="bff7d-165">Booleano de rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="bff7d-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="bff7d-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff7d-166">-ResourceGroupName</span></span>
<span data-ttu-id="bff7d-167">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bff7d-167">Resource Group Name</span></span>

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

### <span data-ttu-id="bff7d-168">-Slot</span><span class="sxs-lookup"><span data-stu-id="bff7d-168">-Slot</span></span>
<span data-ttu-id="bff7d-169">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="bff7d-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bff7d-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="bff7d-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="bff7d-171">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="bff7d-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="bff7d-172">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bff7d-172">-WebApp</span></span>
<span data-ttu-id="bff7d-173">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="bff7d-173">WebApp Object</span></span>

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

### <span data-ttu-id="bff7d-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="bff7d-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="bff7d-175">Booleano habilitados para Web Sockets</span><span class="sxs-lookup"><span data-stu-id="bff7d-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="bff7d-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff7d-176">CommonParameters</span></span>
<span data-ttu-id="bff7d-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff7d-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff7d-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff7d-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff7d-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bff7d-179">INPUTS</span></span>

### <span data-ttu-id="bff7d-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bff7d-180">System.Int32</span></span>

### <span data-ttu-id="bff7d-181">System. String</span><span class="sxs-lookup"><span data-stu-id="bff7d-181">System.String</span></span>

### <span data-ttu-id="bff7d-182">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="bff7d-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bff7d-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bff7d-183">OUTPUTS</span></span>

### <span data-ttu-id="bff7d-184">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="bff7d-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bff7d-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bff7d-185">NOTES</span></span>

## <span data-ttu-id="bff7d-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bff7d-186">RELATED LINKS</span></span>

[<span data-ttu-id="bff7d-187">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bff7d-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="bff7d-188">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bff7d-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="bff7d-189">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bff7d-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="bff7d-190">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bff7d-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="bff7d-191">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bff7d-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="bff7d-192">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bff7d-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="bff7d-193">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bff7d-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
