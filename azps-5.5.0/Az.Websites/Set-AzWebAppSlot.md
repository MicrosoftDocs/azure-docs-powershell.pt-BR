---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116021"
---
# <span data-ttu-id="f919f-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f919f-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="f919f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f919f-102">SYNOPSIS</span></span>
<span data-ttu-id="f919f-103">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f919f-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="f919f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f919f-104">SYNTAX</span></span>

### <span data-ttu-id="f919f-105">S1</span><span class="sxs-lookup"><span data-stu-id="f919f-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f919f-106">S2</span><span class="sxs-lookup"><span data-stu-id="f919f-106">S2</span></span>
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

## <span data-ttu-id="f919f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f919f-107">DESCRIPTION</span></span>
<span data-ttu-id="f919f-108">O **cmdlet Set-AzWebApp** define um Slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f919f-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="f919f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f919f-109">EXAMPLES</span></span>

### <span data-ttu-id="f919f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f919f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="f919f-111">Esse comando altera o plano de serviço de aplicativo associado ao Slot001, no Webapp ContosoWebApp associado ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="f919f-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="f919f-112">Use o link para saber mais sobre como alterar o plano de serviço de aplicativo e as restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="f919f-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="f919f-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="f919f-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="f919f-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f919f-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="f919f-115">Este comando define HttpLoggingEnabled como true para Slot Slot001 pertencente ao Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="f919f-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="f919f-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f919f-116">Example 3</span></span>

<span data-ttu-id="f919f-117">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f919f-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="f919f-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="f919f-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="f919f-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f919f-119">PARAMETERS</span></span>

### <span data-ttu-id="f919f-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="f919f-120">-AlwaysOn</span></span>
<span data-ttu-id="f919f-121">Certifique-se de que o aplicativo Web seja carregado o tempo todo, em vez de ser descarregado após ficar ocioso.</span><span class="sxs-lookup"><span data-stu-id="f919f-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="f919f-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f919f-122">-AppServicePlan</span></span>
<span data-ttu-id="f919f-123">Nome do Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f919f-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="f919f-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="f919f-124">-AppSettings</span></span>
<span data-ttu-id="f919f-125">Tabela Hash de Configurações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f919f-125">App Settings HashTable.</span></span> <span data-ttu-id="f919f-126">As Configurações de Aplicativo existentes serão substituídas, removendo as configurações que não são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="f919f-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="f919f-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f919f-127">-AsJob</span></span>
<span data-ttu-id="f919f-128">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f919f-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f919f-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f919f-129">-AssignIdentity</span></span>
<span data-ttu-id="f919f-130">Habilitar/desabilitar o MSI em um slot existente [VISUALIZAÇÃO]</span><span class="sxs-lookup"><span data-stu-id="f919f-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="f919f-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="f919f-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="f919f-132">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="f919f-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="f919f-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="f919f-133">-AzureStoragePath</span></span>
<span data-ttu-id="f919f-134">Armazenamento do Azure para montar dentro de um Web App para Contêiner.</span><span class="sxs-lookup"><span data-stu-id="f919f-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="f919f-135">Use New-AzureRmWebAppAzureStoragePath para criar</span><span class="sxs-lookup"><span data-stu-id="f919f-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="f919f-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="f919f-136">-ConnectionStrings</span></span>
<span data-ttu-id="f919f-137">HashTable de Cadeias de Conexão</span><span class="sxs-lookup"><span data-stu-id="f919f-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="f919f-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="f919f-138">-ContainerImageName</span></span>
<span data-ttu-id="f919f-139">Nome da Imagem do Contêiner</span><span class="sxs-lookup"><span data-stu-id="f919f-139">Container Image Name</span></span>

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

### <span data-ttu-id="f919f-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="f919f-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="f919f-141">Senha do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="f919f-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="f919f-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="f919f-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="f919f-143">Url do Servidor de Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="f919f-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="f919f-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="f919f-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="f919f-145">Nome de usuário do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="f919f-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="f919f-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="f919f-146">-DefaultDocuments</span></span>
<span data-ttu-id="f919f-147">Matriz de Cadeia de Caracteres de Documentos Padrão</span><span class="sxs-lookup"><span data-stu-id="f919f-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="f919f-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f919f-148">-DefaultProfile</span></span>
<span data-ttu-id="f919f-149">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f919f-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f919f-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f919f-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="f919f-151">Booliana Habilitada para Log de Erros Detalhado</span><span class="sxs-lookup"><span data-stu-id="f919f-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="f919f-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="f919f-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="f919f-153">Habilitar/Desabilitar contêiner de implantação contínua na Web.</span><span class="sxs-lookup"><span data-stu-id="f919f-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="f919f-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="f919f-154">-FtpsState</span></span>
<span data-ttu-id="f919f-155">Definir o valor do estado Ftps para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f919f-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="f919f-156">Valores Permitidos [Todos os Valores Permitidos | Desabilitado | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="f919f-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="f919f-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="f919f-157">-HandlerMappings</span></span>
<span data-ttu-id="f919f-158">Lista de Mapeamentos de Manipuladores</span><span class="sxs-lookup"><span data-stu-id="f919f-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="f919f-159">-httpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f919f-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="f919f-160">Booliana httpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f919f-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="f919f-161">-httpsOnly</span><span class="sxs-lookup"><span data-stu-id="f919f-161">-HttpsOnly</span></span>
<span data-ttu-id="f919f-162">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um slot existente</span><span class="sxs-lookup"><span data-stu-id="f919f-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="f919f-163">-ManagedModlineMode</span><span class="sxs-lookup"><span data-stu-id="f919f-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="f919f-164">Nome do Modo de Pipeline Gerenciado</span><span class="sxs-lookup"><span data-stu-id="f919f-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="f919f-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f919f-165">-MinTlsVersion</span></span>
<span data-ttu-id="f919f-166">A versão mínima de TLS necessária para solicitações SSL.</span><span class="sxs-lookup"><span data-stu-id="f919f-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="f919f-167">Valores permitidos [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="f919f-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="f919f-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="f919f-168">-Name</span></span>
<span data-ttu-id="f919f-169">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="f919f-169">WebApp Name</span></span>

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

### <span data-ttu-id="f919f-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="f919f-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="f919f-171">Versão do Net Framework</span><span class="sxs-lookup"><span data-stu-id="f919f-171">Net Framework Version</span></span>

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

### <span data-ttu-id="f919f-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="f919f-172">-NumberOfWorkers</span></span>
<span data-ttu-id="f919f-173">O número de trabalhadores a serem alocados</span><span class="sxs-lookup"><span data-stu-id="f919f-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="f919f-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="f919f-174">-PhpVersion</span></span>
<span data-ttu-id="f919f-175">Versão Php</span><span class="sxs-lookup"><span data-stu-id="f919f-175">Php Version</span></span>

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

### <span data-ttu-id="f919f-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="f919f-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="f919f-177">Solicitação de rastreamento booliana habilitada</span><span class="sxs-lookup"><span data-stu-id="f919f-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="f919f-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f919f-178">-ResourceGroupName</span></span>
<span data-ttu-id="f919f-179">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f919f-179">Resource Group Name</span></span>

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

### <span data-ttu-id="f919f-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="f919f-180">-Slot</span></span>
<span data-ttu-id="f919f-181">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="f919f-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f919f-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="f919f-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="f919f-183">Usar booliana do Processo do Trabalhador de 32 bits</span><span class="sxs-lookup"><span data-stu-id="f919f-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="f919f-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f919f-184">-WebApp</span></span>
<span data-ttu-id="f919f-185">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="f919f-185">WebApp Object</span></span>

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

### <span data-ttu-id="f919f-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="f919f-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="f919f-187">Booliana Habilitada para Soquetes web</span><span class="sxs-lookup"><span data-stu-id="f919f-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="f919f-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f919f-188">CommonParameters</span></span>
<span data-ttu-id="f919f-189">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f919f-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f919f-190">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f919f-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f919f-191">Entradas</span><span class="sxs-lookup"><span data-stu-id="f919f-191">INPUTS</span></span>

### <span data-ttu-id="f919f-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f919f-192">System.Int32</span></span>

### <span data-ttu-id="f919f-193">System.String</span><span class="sxs-lookup"><span data-stu-id="f919f-193">System.String</span></span>

### <span data-ttu-id="f919f-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f919f-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f919f-195">Saídas</span><span class="sxs-lookup"><span data-stu-id="f919f-195">OUTPUTS</span></span>

### <span data-ttu-id="f919f-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f919f-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f919f-197">Notas</span><span class="sxs-lookup"><span data-stu-id="f919f-197">NOTES</span></span>

## <span data-ttu-id="f919f-198">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f919f-198">RELATED LINKS</span></span>

[<span data-ttu-id="f919f-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f919f-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f919f-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f919f-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="f919f-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f919f-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="f919f-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f919f-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="f919f-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f919f-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="f919f-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f919f-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="f919f-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f919f-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
