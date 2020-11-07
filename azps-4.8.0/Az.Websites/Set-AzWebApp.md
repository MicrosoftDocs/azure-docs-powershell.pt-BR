---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 0120bd19d1c8930129796e47758bd9f91dccfd5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955237"
---
# <span data-ttu-id="d0ce1-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-101">Set-AzWebApp</span></span>

## <span data-ttu-id="d0ce1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ce1-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="d0ce1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0ce1-104">SYNTAX</span></span>

### <span data-ttu-id="d0ce1-105">Eles</span><span class="sxs-lookup"><span data-stu-id="d0ce1-105">S1</span></span>
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

### <span data-ttu-id="d0ce1-106">S2</span><span class="sxs-lookup"><span data-stu-id="d0ce1-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0ce1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0ce1-107">DESCRIPTION</span></span>
<span data-ttu-id="d0ce1-108">O cmdlet **set-AzWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="d0ce1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0ce1-109">EXAMPLES</span></span>

### <span data-ttu-id="d0ce1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0ce1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="d0ce1-111">Esse comando altera o plano appservice associado ao aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d0ce1-112">Use o link para saber mais sobre como alterar o plano appservice e restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="d0ce1-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="d0ce1-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="d0ce1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d0ce1-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="d0ce1-115">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="d0ce1-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="d0ce1-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d0ce1-116">Example 3</span></span>

<span data-ttu-id="d0ce1-117">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="d0ce1-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d0ce1-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="d0ce1-119">OS</span><span class="sxs-lookup"><span data-stu-id="d0ce1-119">PARAMETERS</span></span>

### <span data-ttu-id="d0ce1-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="d0ce1-120">-AlwaysOn</span></span>
<span data-ttu-id="d0ce1-121">Assegure-se de que o aplicativo Web seja carregado o tempo todo, em vez de não ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="d0ce1-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d0ce1-122">-AppServicePlan</span></span>
<span data-ttu-id="d0ce1-123">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d0ce1-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="d0ce1-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="d0ce1-124">-AppSettings</span></span>
<span data-ttu-id="d0ce1-125">HashTable das configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-125">App Settings HashTable.</span></span> <span data-ttu-id="d0ce1-126">As configurações do aplicativo existente serão substituídas, removendo as configurações não fornecidas.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="d0ce1-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0ce1-127">-AsJob</span></span>
<span data-ttu-id="d0ce1-128">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d0ce1-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0ce1-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d0ce1-129">-AssignIdentity</span></span>
<span data-ttu-id="d0ce1-130">Habilitar/desabilitar o MSI em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="d0ce1-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="d0ce1-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="d0ce1-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="d0ce1-132">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="d0ce1-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="d0ce1-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="d0ce1-133">-AzureStoragePath</span></span>
<span data-ttu-id="d0ce1-134">Armazenamento do Azure para montagem dentro de um aplicativo Web para contêiner.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="d0ce1-135">Usar o New-AzureRmWebAppAzureStoragePath para criá-lo</span><span class="sxs-lookup"><span data-stu-id="d0ce1-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="d0ce1-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="d0ce1-136">-ConnectionStrings</span></span>
<span data-ttu-id="d0ce1-137">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="d0ce1-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="d0ce1-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="d0ce1-138">-ContainerImageName</span></span>
<span data-ttu-id="d0ce1-139">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="d0ce1-139">Container Image Name</span></span>

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

### <span data-ttu-id="d0ce1-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="d0ce1-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="d0ce1-141">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="d0ce1-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="d0ce1-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="d0ce1-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="d0ce1-143">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="d0ce1-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="d0ce1-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="d0ce1-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="d0ce1-145">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="d0ce1-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="d0ce1-146">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="d0ce1-146">-DefaultDocuments</span></span>
<span data-ttu-id="d0ce1-147">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="d0ce1-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="d0ce1-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ce1-148">-DefaultProfile</span></span>
<span data-ttu-id="d0ce1-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0ce1-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d0ce1-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="d0ce1-151">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="d0ce1-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="d0ce1-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="d0ce1-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="d0ce1-153">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="d0ce1-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="d0ce1-154">-Ftpsstate</span><span class="sxs-lookup"><span data-stu-id="d0ce1-154">-FtpsState</span></span>
<span data-ttu-id="d0ce1-155">Defina o valor do estado de FTPS para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="d0ce1-156">Valores permitidos [permitidos | Desativado | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="d0ce1-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="d0ce1-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="d0ce1-157">-HandlerMappings</span></span>
<span data-ttu-id="d0ce1-158">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="d0ce1-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="d0ce1-159">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="d0ce1-159">-HostNames</span></span>
<span data-ttu-id="d0ce1-160">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="d0ce1-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d0ce1-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="d0ce1-162">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="d0ce1-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="d0ce1-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d0ce1-163">-HttpsOnly</span></span>
<span data-ttu-id="d0ce1-164">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="d0ce1-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="d0ce1-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="d0ce1-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="d0ce1-166">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="d0ce1-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="d0ce1-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d0ce1-167">-MinTlsVersion</span></span>
<span data-ttu-id="d0ce1-168">A versão mínima do TLS necessária para solicitações SSL.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="d0ce1-169">Valores permitidos [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="d0ce1-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="d0ce1-170">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0ce1-170">-Name</span></span>
<span data-ttu-id="d0ce1-171">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-171">WebApp Name</span></span>

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

### <span data-ttu-id="d0ce1-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="d0ce1-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="d0ce1-173">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d0ce1-173">Net Framework Version</span></span>

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

### <span data-ttu-id="d0ce1-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="d0ce1-174">-NumberOfWorkers</span></span>
<span data-ttu-id="d0ce1-175">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="d0ce1-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="d0ce1-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="d0ce1-176">-PhpVersion</span></span>
<span data-ttu-id="d0ce1-177">Versão do php</span><span class="sxs-lookup"><span data-stu-id="d0ce1-177">Php Version</span></span>

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

### <span data-ttu-id="d0ce1-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="d0ce1-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="d0ce1-179">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="d0ce1-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="d0ce1-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0ce1-180">-ResourceGroupName</span></span>
<span data-ttu-id="d0ce1-181">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d0ce1-181">Resource Group Name</span></span>

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

### <span data-ttu-id="d0ce1-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="d0ce1-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="d0ce1-183">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d0ce1-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="d0ce1-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-184">-WebApp</span></span>
<span data-ttu-id="d0ce1-185">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-185">WebApp Object</span></span>

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

### <span data-ttu-id="d0ce1-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0ce1-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="d0ce1-187">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="d0ce1-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="d0ce1-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ce1-188">CommonParameters</span></span>
<span data-ttu-id="d0ce1-189">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ce1-190">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0ce1-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ce1-191">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0ce1-191">INPUTS</span></span>

### <span data-ttu-id="d0ce1-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d0ce1-192">System.Int32</span></span>

### <span data-ttu-id="d0ce1-193">System. String</span><span class="sxs-lookup"><span data-stu-id="d0ce1-193">System.String</span></span>

### <span data-ttu-id="d0ce1-194">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d0ce1-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d0ce1-195">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0ce1-195">OUTPUTS</span></span>

### <span data-ttu-id="d0ce1-196">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d0ce1-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d0ce1-197">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0ce1-197">NOTES</span></span>
<span data-ttu-id="d0ce1-198">Abaixo o cmdlet fornecido vai ajudá-lo a atualizar o Azure Web App para o **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="d0ce1-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="d0ce1-199">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-Propertyobject $PropertiesObject-ResourceGroupName "Default-Web-Oesteus"-ResourceType Microsoft. Web/sites/config-resourceName "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="d0ce1-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="d0ce1-200">Substitua os valores de Default-Web-Oesteus pelo nome do grupo de recursos do webapp e do ContosoWebApp com o nome do webapp.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="d0ce1-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0ce1-201">RELATED LINKS</span></span>

[<span data-ttu-id="d0ce1-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d0ce1-203">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d0ce1-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d0ce1-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d0ce1-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d0ce1-207">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d0ce1-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="d0ce1-208">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="d0ce1-208">New-AzResource</span></span>](./New-AzResource.md)
