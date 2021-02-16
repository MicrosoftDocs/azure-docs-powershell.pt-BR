---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 46c5dae54bf4f59556e62256797a43221d0650b7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412343"
---
# <span data-ttu-id="e49b6-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-101">Set-AzWebApp</span></span>

## <span data-ttu-id="e49b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e49b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e49b6-103">Modifica um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e49b6-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="e49b6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e49b6-104">SYNTAX</span></span>

### <span data-ttu-id="e49b6-105">S1</span><span class="sxs-lookup"><span data-stu-id="e49b6-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e49b6-106">S2</span><span class="sxs-lookup"><span data-stu-id="e49b6-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e49b6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e49b6-107">DESCRIPTION</span></span>
<span data-ttu-id="e49b6-108">O **cmdlet Set-AzWebApp** define um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e49b6-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="e49b6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e49b6-109">EXAMPLES</span></span>

### <span data-ttu-id="e49b6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e49b6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="e49b6-111">Esse comando altera o plano de serviço de aplicativo associado ao Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e49b6-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="e49b6-112">Use o link para saber mais sobre como alterar o plano de serviço de aplicativo e as restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="e49b6-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="e49b6-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="e49b6-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="e49b6-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e49b6-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="e49b6-115">Este comando define HttpLoggingEnabled como true para o Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="e49b6-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="e49b6-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e49b6-116">Example 3</span></span>

<span data-ttu-id="e49b6-117">Modifica um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e49b6-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="e49b6-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e49b6-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="e49b6-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e49b6-119">PARAMETERS</span></span>

### <span data-ttu-id="e49b6-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="e49b6-120">-AlwaysOn</span></span>
<span data-ttu-id="e49b6-121">Certifique-se de que o aplicativo Web seja carregado o tempo todo, em vez de ser descarregado após ficar ocioso.</span><span class="sxs-lookup"><span data-stu-id="e49b6-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="e49b6-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e49b6-122">-AppServicePlan</span></span>
<span data-ttu-id="e49b6-123">Nome do Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e49b6-123">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="e49b6-124">-AppSettings</span></span>
<span data-ttu-id="e49b6-125">Tabela Hash de Configurações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e49b6-125">App Settings HashTable.</span></span> <span data-ttu-id="e49b6-126">As Configurações de Aplicativo existentes serão substituídas, removendo as configurações que não são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="e49b6-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e49b6-127">-AsJob</span></span>
<span data-ttu-id="e49b6-128">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e49b6-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e49b6-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e49b6-129">-AssignIdentity</span></span>
<span data-ttu-id="e49b6-130">Habilitar/desabilitar o MSI em um aplicativo web ou functionapp do azure existente</span><span class="sxs-lookup"><span data-stu-id="e49b6-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="e49b6-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="e49b6-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="e49b6-132">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="e49b6-132">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="e49b6-133">-AzureStoragePath</span></span>
<span data-ttu-id="e49b6-134">Armazenamento do Azure para montar dentro de um Web App para Contêiner.</span><span class="sxs-lookup"><span data-stu-id="e49b6-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="e49b6-135">Use New-AzureRmWebAppAzureStoragePath para criar</span><span class="sxs-lookup"><span data-stu-id="e49b6-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="e49b6-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="e49b6-136">-ConnectionStrings</span></span>
<span data-ttu-id="e49b6-137">HashTable de Cadeias de Conexão</span><span class="sxs-lookup"><span data-stu-id="e49b6-137">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="e49b6-138">-ContainerImageName</span></span>
<span data-ttu-id="e49b6-139">Nome da Imagem do Contêiner</span><span class="sxs-lookup"><span data-stu-id="e49b6-139">Container Image Name</span></span>

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

### <span data-ttu-id="e49b6-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="e49b6-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="e49b6-141">Senha do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="e49b6-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="e49b6-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="e49b6-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="e49b6-143">Url do Servidor de Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="e49b6-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="e49b6-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="e49b6-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="e49b6-145">Nome de usuário do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="e49b6-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="e49b6-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="e49b6-146">-DefaultDocuments</span></span>
<span data-ttu-id="e49b6-147">Matriz de Cadeia de Caracteres de Documentos Padrão</span><span class="sxs-lookup"><span data-stu-id="e49b6-147">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49b6-148">-DefaultProfile</span></span>
<span data-ttu-id="e49b6-149">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e49b6-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e49b6-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e49b6-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="e49b6-151">Booliana Habilitada para Log de Erros Detalhado</span><span class="sxs-lookup"><span data-stu-id="e49b6-151">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="e49b6-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="e49b6-153">Habilitar/Desabilitar contêiner de implantação contínua na Web.</span><span class="sxs-lookup"><span data-stu-id="e49b6-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="e49b6-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="e49b6-154">-FtpsState</span></span>
<span data-ttu-id="e49b6-155">Definir o valor do estado Ftps para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e49b6-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="e49b6-156">Valores Permitidos [Todos os Valores Permitidos | Desabilitado | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="e49b6-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="e49b6-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="e49b6-157">-HandlerMappings</span></span>
<span data-ttu-id="e49b6-158">Lista de Mapeamentos de Manipuladores</span><span class="sxs-lookup"><span data-stu-id="e49b6-158">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-159">-Nomes de Host</span><span class="sxs-lookup"><span data-stu-id="e49b6-159">-HostNames</span></span>
<span data-ttu-id="e49b6-160">Matriz de cadeia de caracteres Nomes de Host do WebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-160">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-161">-httpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e49b6-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="e49b6-162">Booliana httpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e49b6-162">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-163">-httpsOnly</span><span class="sxs-lookup"><span data-stu-id="e49b6-163">-HttpsOnly</span></span>
<span data-ttu-id="e49b6-164">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um aplicativo web ou functionapp do azure existente</span><span class="sxs-lookup"><span data-stu-id="e49b6-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="e49b6-165">-ManagedModlineMode</span><span class="sxs-lookup"><span data-stu-id="e49b6-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="e49b6-166">Nome do Modo de Pipeline Gerenciado</span><span class="sxs-lookup"><span data-stu-id="e49b6-166">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e49b6-167">-MinTlsVersion</span></span>
<span data-ttu-id="e49b6-168">A versão mínima de TLS necessária para solicitações SSL.</span><span class="sxs-lookup"><span data-stu-id="e49b6-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="e49b6-169">Valores permitidos [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="e49b6-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="e49b6-170">-Nome</span><span class="sxs-lookup"><span data-stu-id="e49b6-170">-Name</span></span>
<span data-ttu-id="e49b6-171">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="e49b6-171">WebApp Name</span></span>

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

### <span data-ttu-id="e49b6-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="e49b6-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="e49b6-173">Versão do Net Framework</span><span class="sxs-lookup"><span data-stu-id="e49b6-173">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="e49b6-174">-NumberOfWorkers</span></span>
<span data-ttu-id="e49b6-175">O número de trabalhadores a serem alocados</span><span class="sxs-lookup"><span data-stu-id="e49b6-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="e49b6-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="e49b6-176">-PhpVersion</span></span>
<span data-ttu-id="e49b6-177">Versão Php</span><span class="sxs-lookup"><span data-stu-id="e49b6-177">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="e49b6-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="e49b6-179">Solicitar Rastreamento Habilitado</span><span class="sxs-lookup"><span data-stu-id="e49b6-179">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49b6-180">-ResourceGroupName</span></span>
<span data-ttu-id="e49b6-181">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e49b6-181">Resource Group Name</span></span>

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

### <span data-ttu-id="e49b6-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="e49b6-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="e49b6-183">Usar booliana do Processo do Trabalhador de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e49b6-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="e49b6-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-184">-WebApp</span></span>
<span data-ttu-id="e49b6-185">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-185">WebApp Object</span></span>

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

### <span data-ttu-id="e49b6-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e49b6-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="e49b6-187">Booliana WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e49b6-187">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49b6-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49b6-188">CommonParameters</span></span>
<span data-ttu-id="e49b6-189">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e49b6-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49b6-190">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e49b6-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49b6-191">Entradas</span><span class="sxs-lookup"><span data-stu-id="e49b6-191">INPUTS</span></span>

### <span data-ttu-id="e49b6-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e49b6-192">System.Int32</span></span>

### <span data-ttu-id="e49b6-193">System.String</span><span class="sxs-lookup"><span data-stu-id="e49b6-193">System.String</span></span>

### <span data-ttu-id="e49b6-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e49b6-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e49b6-195">Saídas</span><span class="sxs-lookup"><span data-stu-id="e49b6-195">OUTPUTS</span></span>

### <span data-ttu-id="e49b6-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e49b6-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e49b6-197">Notas</span><span class="sxs-lookup"><span data-stu-id="e49b6-197">NOTES</span></span>
<span data-ttu-id="e49b6-198">O cmdlet abaixo fornecido ajudará você a atualizar o Azure Web App para **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="e49b6-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="e49b6-199">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadados" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="e49b6-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="e49b6-200">Substitua os valores de Default-Web-WestUS pelo nome do grupo de recursos do webapp e contosoWebApp pelo nome do webapp.</span><span class="sxs-lookup"><span data-stu-id="e49b6-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="e49b6-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e49b6-201">RELATED LINKS</span></span>

[<span data-ttu-id="e49b6-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e49b6-203">Novo-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e49b6-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e49b6-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e49b6-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e49b6-207">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e49b6-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

