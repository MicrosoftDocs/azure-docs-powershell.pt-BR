---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774178"
---
# <span data-ttu-id="747de-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="747de-101">Set-AzWebApp</span></span>

## <span data-ttu-id="747de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="747de-102">SYNOPSIS</span></span>
<span data-ttu-id="747de-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="747de-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="747de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="747de-104">SYNTAX</span></span>

### <span data-ttu-id="747de-105">Eles</span><span class="sxs-lookup"><span data-stu-id="747de-105">S1</span></span>
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
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="747de-106">S2</span><span class="sxs-lookup"><span data-stu-id="747de-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="747de-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="747de-107">DESCRIPTION</span></span>
<span data-ttu-id="747de-108">O cmdlet **set-AzWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="747de-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="747de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="747de-109">EXAMPLES</span></span>

### <span data-ttu-id="747de-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="747de-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="747de-111">Esse comando altera o plano appservice associado ao aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="747de-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="747de-112">Use o link para saber mais sobre como alterar o plano appservice e restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="747de-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="747de-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="747de-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="747de-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="747de-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="747de-115">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="747de-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="747de-116">OS</span><span class="sxs-lookup"><span data-stu-id="747de-116">PARAMETERS</span></span>

### <span data-ttu-id="747de-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="747de-117">-AppServicePlan</span></span>
<span data-ttu-id="747de-118">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="747de-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="747de-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="747de-119">-AppSettings</span></span>
<span data-ttu-id="747de-120">HashTable das configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="747de-120">App Settings HashTable.</span></span> <span data-ttu-id="747de-121">As configurações do aplicativo existente serão substituídas, removendo as configurações não fornecidas.</span><span class="sxs-lookup"><span data-stu-id="747de-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="747de-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="747de-122">-AsJob</span></span>
<span data-ttu-id="747de-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="747de-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="747de-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="747de-124">-AssignIdentity</span></span>
<span data-ttu-id="747de-125">Habilitar/desabilitar o MSI em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="747de-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="747de-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="747de-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="747de-127">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="747de-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="747de-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="747de-128">-AzureStoragePath</span></span>
<span data-ttu-id="747de-129">Armazenamento do Azure para montagem dentro de um aplicativo Web para contêiner.</span><span class="sxs-lookup"><span data-stu-id="747de-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="747de-130">Usar o New-AzureRmWebAppAzureStoragePath para criá-lo</span><span class="sxs-lookup"><span data-stu-id="747de-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="747de-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="747de-131">-ConnectionStrings</span></span>
<span data-ttu-id="747de-132">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="747de-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="747de-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="747de-133">-ContainerImageName</span></span>
<span data-ttu-id="747de-134">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="747de-134">Container Image Name</span></span>

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

### <span data-ttu-id="747de-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="747de-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="747de-136">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="747de-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="747de-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="747de-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="747de-138">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="747de-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="747de-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="747de-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="747de-140">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="747de-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="747de-141">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="747de-141">-DefaultDocuments</span></span>
<span data-ttu-id="747de-142">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="747de-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="747de-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747de-143">-DefaultProfile</span></span>
<span data-ttu-id="747de-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="747de-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="747de-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="747de-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="747de-146">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="747de-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="747de-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="747de-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="747de-148">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="747de-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="747de-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="747de-149">-HandlerMappings</span></span>
<span data-ttu-id="747de-150">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="747de-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="747de-151">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="747de-151">-HostNames</span></span>
<span data-ttu-id="747de-152">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="747de-152">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="747de-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="747de-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="747de-154">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="747de-154">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="747de-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="747de-155">-HttpsOnly</span></span>
<span data-ttu-id="747de-156">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="747de-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="747de-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="747de-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="747de-158">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="747de-158">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="747de-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="747de-159">-Name</span></span>
<span data-ttu-id="747de-160">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="747de-160">WebApp Name</span></span>

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

### <span data-ttu-id="747de-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="747de-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="747de-162">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="747de-162">Net Framework Version</span></span>

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

### <span data-ttu-id="747de-163">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="747de-163">-NumberOfWorkers</span></span>
<span data-ttu-id="747de-164">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="747de-164">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="747de-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="747de-165">-PhpVersion</span></span>
<span data-ttu-id="747de-166">Versão do php</span><span class="sxs-lookup"><span data-stu-id="747de-166">Php Version</span></span>

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

### <span data-ttu-id="747de-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="747de-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="747de-168">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="747de-168">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="747de-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="747de-169">-ResourceGroupName</span></span>
<span data-ttu-id="747de-170">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="747de-170">Resource Group Name</span></span>

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

### <span data-ttu-id="747de-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="747de-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="747de-172">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="747de-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="747de-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="747de-173">-WebApp</span></span>
<span data-ttu-id="747de-174">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="747de-174">WebApp Object</span></span>

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

### <span data-ttu-id="747de-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="747de-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="747de-176">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="747de-176">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="747de-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747de-177">CommonParameters</span></span>
<span data-ttu-id="747de-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747de-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747de-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="747de-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747de-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="747de-180">INPUTS</span></span>

### <span data-ttu-id="747de-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="747de-181">System.Int32</span></span>

### <span data-ttu-id="747de-182">System. String</span><span class="sxs-lookup"><span data-stu-id="747de-182">System.String</span></span>

### <span data-ttu-id="747de-183">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="747de-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="747de-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="747de-184">OUTPUTS</span></span>

### <span data-ttu-id="747de-185">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="747de-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="747de-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="747de-186">NOTES</span></span>

## <span data-ttu-id="747de-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="747de-187">RELATED LINKS</span></span>

[<span data-ttu-id="747de-188">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="747de-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="747de-189">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="747de-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="747de-190">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="747de-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="747de-191">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="747de-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="747de-192">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="747de-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="747de-193">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="747de-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
