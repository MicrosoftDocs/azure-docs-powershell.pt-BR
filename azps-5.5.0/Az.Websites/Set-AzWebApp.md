---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116024"
---
# <span data-ttu-id="157a4-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-101">Set-AzWebApp</span></span>

## <span data-ttu-id="157a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="157a4-102">SYNOPSIS</span></span>
<span data-ttu-id="157a4-103">Modifica um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="157a4-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="157a4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="157a4-104">SYNTAX</span></span>

### <span data-ttu-id="157a4-105">S1</span><span class="sxs-lookup"><span data-stu-id="157a4-105">S1</span></span>
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

### <span data-ttu-id="157a4-106">S2</span><span class="sxs-lookup"><span data-stu-id="157a4-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="157a4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="157a4-107">DESCRIPTION</span></span>
<span data-ttu-id="157a4-108">O **cmdlet Set-AzWebApp** define um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="157a4-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="157a4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="157a4-109">EXAMPLES</span></span>

### <span data-ttu-id="157a4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="157a4-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="157a4-111">Esse comando altera o plano de serviço de aplicativo associado ao Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="157a4-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="157a4-112">Use o link para saber mais sobre como alterar o plano de serviço de aplicativo e as restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="157a4-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="157a4-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="157a4-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="157a4-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="157a4-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="157a4-115">Este comando define HttpLoggingEnabled como true para o Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="157a4-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="157a4-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="157a4-116">Example 3</span></span>

<span data-ttu-id="157a4-117">Modifica um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="157a4-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="157a4-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="157a4-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="157a4-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="157a4-119">Example 4</span></span>

<span data-ttu-id="157a4-120">O exemplo a seguir cria uma cadeia de conexão chamada myConnectionString para ContosoWebApp do Web App.</span><span class="sxs-lookup"><span data-stu-id="157a4-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="157a4-121">Isso substitui todas as cadeias de conexão existentes para ContosoWebApp do Web App.</span><span class="sxs-lookup"><span data-stu-id="157a4-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="157a4-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="157a4-122">PARAMETERS</span></span>

### <span data-ttu-id="157a4-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="157a4-123">-AlwaysOn</span></span>
<span data-ttu-id="157a4-124">Certifique-se de que o aplicativo Web seja carregado o tempo todo, em vez de ser descarregado após ficar ocioso.</span><span class="sxs-lookup"><span data-stu-id="157a4-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="157a4-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="157a4-125">-AppServicePlan</span></span>
<span data-ttu-id="157a4-126">Nome do Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="157a4-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="157a4-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="157a4-127">-AppSettings</span></span>
<span data-ttu-id="157a4-128">Tabela Hash de Configurações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="157a4-128">App Settings HashTable.</span></span> <span data-ttu-id="157a4-129">As Configurações de Aplicativo existentes serão substituídas, removendo as configurações que não são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="157a4-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="157a4-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="157a4-130">-AsJob</span></span>
<span data-ttu-id="157a4-131">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="157a4-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="157a4-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="157a4-132">-AssignIdentity</span></span>
<span data-ttu-id="157a4-133">Habilitar/desabilitar o MSI em um aplicativo web ou functionapp do azure existente</span><span class="sxs-lookup"><span data-stu-id="157a4-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="157a4-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="157a4-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="157a4-135">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="157a4-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="157a4-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="157a4-136">-AzureStoragePath</span></span>
<span data-ttu-id="157a4-137">Armazenamento do Azure para montar dentro de um Web App para Contêiner.</span><span class="sxs-lookup"><span data-stu-id="157a4-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="157a4-138">Use New-AzureRmWebAppAzureStoragePath para criar</span><span class="sxs-lookup"><span data-stu-id="157a4-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="157a4-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="157a4-139">-ConnectionStrings</span></span>
<span data-ttu-id="157a4-140">HashTable de Cadeias de Conexão</span><span class="sxs-lookup"><span data-stu-id="157a4-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="157a4-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="157a4-141">-ContainerImageName</span></span>
<span data-ttu-id="157a4-142">Nome da Imagem do Contêiner</span><span class="sxs-lookup"><span data-stu-id="157a4-142">Container Image Name</span></span>

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

### <span data-ttu-id="157a4-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="157a4-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="157a4-144">Senha do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="157a4-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="157a4-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="157a4-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="157a4-146">Url do Servidor de Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="157a4-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="157a4-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="157a4-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="157a4-148">Nome de usuário do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="157a4-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="157a4-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="157a4-149">-DefaultDocuments</span></span>
<span data-ttu-id="157a4-150">Matriz de Cadeia de Caracteres de Documentos Padrão</span><span class="sxs-lookup"><span data-stu-id="157a4-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="157a4-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157a4-151">-DefaultProfile</span></span>
<span data-ttu-id="157a4-152">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="157a4-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="157a4-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="157a4-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="157a4-154">Booliana Habilitada para Log de Erros Detalhado</span><span class="sxs-lookup"><span data-stu-id="157a4-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="157a4-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="157a4-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="157a4-156">Habilitar/Desabilitar contêiner de implantação contínua na Web.</span><span class="sxs-lookup"><span data-stu-id="157a4-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="157a4-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="157a4-157">-FtpsState</span></span>
<span data-ttu-id="157a4-158">Definir o valor do estado Ftps para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="157a4-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="157a4-159">Valores Permitidos [Todos os Valores Permitidos | Desabilitado | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="157a4-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="157a4-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="157a4-160">-HandlerMappings</span></span>
<span data-ttu-id="157a4-161">Lista de Mapeamentos de Manipuladores</span><span class="sxs-lookup"><span data-stu-id="157a4-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="157a4-162">-Nomes de Host</span><span class="sxs-lookup"><span data-stu-id="157a4-162">-HostNames</span></span>
<span data-ttu-id="157a4-163">Matriz de cadeia de caracteres Nomes de Host do WebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="157a4-164">-httpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="157a4-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="157a4-165">Booliana httpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="157a4-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="157a4-166">-httpsOnly</span><span class="sxs-lookup"><span data-stu-id="157a4-166">-HttpsOnly</span></span>
<span data-ttu-id="157a4-167">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um aplicativo web ou functionapp do Azure existente</span><span class="sxs-lookup"><span data-stu-id="157a4-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="157a4-168">-ManagedModlineMode</span><span class="sxs-lookup"><span data-stu-id="157a4-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="157a4-169">Nome do Modo de Pipeline Gerenciado</span><span class="sxs-lookup"><span data-stu-id="157a4-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="157a4-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="157a4-170">-MinTlsVersion</span></span>
<span data-ttu-id="157a4-171">A versão mínima de TLS necessária para solicitações SSL.</span><span class="sxs-lookup"><span data-stu-id="157a4-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="157a4-172">Valores permitidos [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="157a4-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="157a4-173">-Nome</span><span class="sxs-lookup"><span data-stu-id="157a4-173">-Name</span></span>
<span data-ttu-id="157a4-174">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="157a4-174">WebApp Name</span></span>

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

### <span data-ttu-id="157a4-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="157a4-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="157a4-176">Versão do Net Framework</span><span class="sxs-lookup"><span data-stu-id="157a4-176">Net Framework Version</span></span>

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

### <span data-ttu-id="157a4-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="157a4-177">-NumberOfWorkers</span></span>
<span data-ttu-id="157a4-178">O número de trabalhadores a serem alocados</span><span class="sxs-lookup"><span data-stu-id="157a4-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="157a4-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="157a4-179">-PhpVersion</span></span>
<span data-ttu-id="157a4-180">Versão Php</span><span class="sxs-lookup"><span data-stu-id="157a4-180">Php Version</span></span>

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

### <span data-ttu-id="157a4-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="157a4-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="157a4-182">Solicitar Rastreamento Habilitado</span><span class="sxs-lookup"><span data-stu-id="157a4-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="157a4-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157a4-183">-ResourceGroupName</span></span>
<span data-ttu-id="157a4-184">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="157a4-184">Resource Group Name</span></span>

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

### <span data-ttu-id="157a4-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="157a4-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="157a4-186">Usar booliana do Processo do Trabalhador de 32 bits</span><span class="sxs-lookup"><span data-stu-id="157a4-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="157a4-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-187">-WebApp</span></span>
<span data-ttu-id="157a4-188">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-188">WebApp Object</span></span>

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

### <span data-ttu-id="157a4-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="157a4-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="157a4-190">Booliana WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="157a4-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="157a4-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157a4-191">CommonParameters</span></span>
<span data-ttu-id="157a4-192">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157a4-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157a4-193">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="157a4-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157a4-194">Entradas</span><span class="sxs-lookup"><span data-stu-id="157a4-194">INPUTS</span></span>

### <span data-ttu-id="157a4-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="157a4-195">System.Int32</span></span>

### <span data-ttu-id="157a4-196">System.String</span><span class="sxs-lookup"><span data-stu-id="157a4-196">System.String</span></span>

### <span data-ttu-id="157a4-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="157a4-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="157a4-198">Saídas</span><span class="sxs-lookup"><span data-stu-id="157a4-198">OUTPUTS</span></span>

### <span data-ttu-id="157a4-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="157a4-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="157a4-200">Notas</span><span class="sxs-lookup"><span data-stu-id="157a4-200">NOTES</span></span>
<span data-ttu-id="157a4-201">O cmdlet abaixo fornecido ajudará você a atualizar o Azure Web App para **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="157a4-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="157a4-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadados" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="157a4-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="157a4-203">Substitua os valores de Default-Web-WestUS pelo nome do grupo de recursos do webapp e contosoWebApp pelo nome do webapp.</span><span class="sxs-lookup"><span data-stu-id="157a4-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="157a4-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="157a4-204">RELATED LINKS</span></span>

[<span data-ttu-id="157a4-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="157a4-206">Novo-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="157a4-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="157a4-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="157a4-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="157a4-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="157a4-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="157a4-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="157a4-211">New-AzResource</span></span>](./New-AzResource.md)
