---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429985"
---
# <span data-ttu-id="5ace5-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="5ace5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ace5-102">SYNOPSIS</span></span>
<span data-ttu-id="5ace5-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ace5-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ace5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ace5-104">SYNTAX</span></span>

### <span data-ttu-id="5ace5-105">Eles</span><span class="sxs-lookup"><span data-stu-id="5ace5-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ace5-106">S2</span><span class="sxs-lookup"><span data-stu-id="5ace5-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ace5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ace5-107">DESCRIPTION</span></span>
<span data-ttu-id="5ace5-108">O cmdlet **set-AzureRmWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ace5-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="5ace5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ace5-109">EXAMPLES</span></span>

### <span data-ttu-id="5ace5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ace5-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="5ace5-111">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="5ace5-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5ace5-112">OS</span><span class="sxs-lookup"><span data-stu-id="5ace5-112">PARAMETERS</span></span>

### <span data-ttu-id="5ace5-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ace5-113">-AppServicePlan</span></span>
<span data-ttu-id="5ace5-114">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="5ace5-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="5ace5-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="5ace5-115">-AppSettings</span></span>
<span data-ttu-id="5ace5-116">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5ace5-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="5ace5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ace5-117">-AsJob</span></span>
<span data-ttu-id="5ace5-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5ace5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ace5-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5ace5-119">-AssignIdentity</span></span>
<span data-ttu-id="5ace5-120">Habilitar/desabilitar o MSI em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="5ace5-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="5ace5-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="5ace5-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="5ace5-122">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="5ace5-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="5ace5-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="5ace5-123">-ConnectionStrings</span></span>
<span data-ttu-id="5ace5-124">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="5ace5-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="5ace5-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="5ace5-125">-ContainerImageName</span></span>
<span data-ttu-id="5ace5-126">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="5ace5-126">Container Image Name</span></span>

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

### <span data-ttu-id="5ace5-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="5ace5-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="5ace5-128">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="5ace5-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="5ace5-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="5ace5-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="5ace5-130">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="5ace5-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="5ace5-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="5ace5-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="5ace5-132">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="5ace5-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="5ace5-133">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="5ace5-133">-DefaultDocuments</span></span>
<span data-ttu-id="5ace5-134">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="5ace5-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="5ace5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ace5-135">-DefaultProfile</span></span>
<span data-ttu-id="5ace5-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ace5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ace5-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="5ace5-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="5ace5-138">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="5ace5-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="5ace5-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="5ace5-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="5ace5-140">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="5ace5-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="5ace5-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="5ace5-141">-HandlerMappings</span></span>
<span data-ttu-id="5ace5-142">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="5ace5-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="5ace5-143">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="5ace5-143">-HostNames</span></span>
<span data-ttu-id="5ace5-144">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-144">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="5ace5-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="5ace5-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="5ace5-146">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="5ace5-146">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="5ace5-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5ace5-147">-HttpsOnly</span></span>
<span data-ttu-id="5ace5-148">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="5ace5-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="5ace5-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="5ace5-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="5ace5-150">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="5ace5-150">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="5ace5-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ace5-151">-Name</span></span>
<span data-ttu-id="5ace5-152">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-152">WebApp Name</span></span>

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

### <span data-ttu-id="5ace5-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="5ace5-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="5ace5-154">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="5ace5-154">Net Framework Version</span></span>

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

### <span data-ttu-id="5ace5-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="5ace5-155">-NumberOfWorkers</span></span>
<span data-ttu-id="5ace5-156">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="5ace5-156">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="5ace5-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="5ace5-157">-PhpVersion</span></span>
<span data-ttu-id="5ace5-158">Versão do php</span><span class="sxs-lookup"><span data-stu-id="5ace5-158">Php Version</span></span>

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

### <span data-ttu-id="5ace5-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="5ace5-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="5ace5-160">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="5ace5-160">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="5ace5-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ace5-161">-ResourceGroupName</span></span>
<span data-ttu-id="5ace5-162">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5ace5-162">Resource Group Name</span></span>

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

### <span data-ttu-id="5ace5-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="5ace5-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="5ace5-164">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="5ace5-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="5ace5-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-165">-WebApp</span></span>
<span data-ttu-id="5ace5-166">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-166">WebApp Object</span></span>

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

### <span data-ttu-id="5ace5-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="5ace5-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="5ace5-168">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="5ace5-168">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="5ace5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ace5-169">CommonParameters</span></span>
<span data-ttu-id="5ace5-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ace5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ace5-171">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ace5-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ace5-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ace5-172">INPUTS</span></span>

### <span data-ttu-id="5ace5-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5ace5-173">System.Int32</span></span>
<span data-ttu-id="5ace5-174">Parâmetros: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ace5-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="5ace5-175">System. String</span><span class="sxs-lookup"><span data-stu-id="5ace5-175">System.String</span></span>

### <span data-ttu-id="5ace5-176">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="5ace5-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="5ace5-177">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ace5-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="5ace5-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ace5-178">OUTPUTS</span></span>

### <span data-ttu-id="5ace5-179">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="5ace5-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="5ace5-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ace5-180">NOTES</span></span>

## <span data-ttu-id="5ace5-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ace5-181">RELATED LINKS</span></span>

[<span data-ttu-id="5ace5-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="5ace5-183">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="5ace5-184">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="5ace5-185">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="5ace5-186">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="5ace5-187">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5ace5-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
