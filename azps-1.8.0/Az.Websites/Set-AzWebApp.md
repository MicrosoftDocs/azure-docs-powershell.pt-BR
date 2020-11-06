---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598298"
---
# <span data-ttu-id="1895d-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-101">Set-AzWebApp</span></span>



## <span data-ttu-id="1895d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1895d-102">SYNOPSIS</span></span>

<span data-ttu-id="1895d-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="1895d-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="1895d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1895d-104">SYNTAX</span></span>



### <span data-ttu-id="1895d-105">Eles</span><span class="sxs-lookup"><span data-stu-id="1895d-105">S1</span></span>

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



### <span data-ttu-id="1895d-106">S2</span><span class="sxs-lookup"><span data-stu-id="1895d-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="1895d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1895d-107">DESCRIPTION</span></span>

<span data-ttu-id="1895d-108">O cmdlet **set-AzWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="1895d-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="1895d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1895d-109">EXAMPLES</span></span>



### <span data-ttu-id="1895d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1895d-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="1895d-111">Esse comando altera o plano appservice associado ao aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="1895d-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1895d-112">Use o link para limpar e saber mais sobre como alterar o plano appservice e restrições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="1895d-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="1895d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1895d-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="1895d-114">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="1895d-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="1895d-115">OS</span><span class="sxs-lookup"><span data-stu-id="1895d-115">PARAMETERS</span></span>



### <span data-ttu-id="1895d-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1895d-116">-AppServicePlan</span></span>

<span data-ttu-id="1895d-117">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1895d-117">App Service Plan Name</span></span>



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



### <span data-ttu-id="1895d-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="1895d-118">-AppSettings</span></span>

<span data-ttu-id="1895d-119">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="1895d-119">App Settings HashTable</span></span>



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



### <span data-ttu-id="1895d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1895d-120">-AsJob</span></span>

<span data-ttu-id="1895d-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1895d-121">Run cmdlet in the background</span></span>



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



### <span data-ttu-id="1895d-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1895d-122">-AssignIdentity</span></span>

<span data-ttu-id="1895d-123">Habilitar/desabilitar o MSI em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="1895d-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="1895d-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="1895d-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="1895d-125">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="1895d-125">Destination slot name for auto swap</span></span>



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



### <span data-ttu-id="1895d-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="1895d-126">-AzureStoragePath</span></span>

<span data-ttu-id="1895d-127">Armazenamento do Azure para montagem dentro de um aplicativo Web para contêiner.</span><span class="sxs-lookup"><span data-stu-id="1895d-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="1895d-128">Usar o New-AzureRmWebAppAzureStoragePath para criá-lo</span><span class="sxs-lookup"><span data-stu-id="1895d-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



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



### <span data-ttu-id="1895d-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="1895d-129">-ConnectionStrings</span></span>

<span data-ttu-id="1895d-130">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="1895d-130">Connection Strings HashTable</span></span>



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



### <span data-ttu-id="1895d-131">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="1895d-131">-ContainerImageName</span></span>

<span data-ttu-id="1895d-132">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="1895d-132">Container Image Name</span></span>



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



### <span data-ttu-id="1895d-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="1895d-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="1895d-134">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="1895d-134">Private Container Registry Password</span></span>



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



### <span data-ttu-id="1895d-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="1895d-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="1895d-136">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="1895d-136">Private Container Registry Server Url</span></span>



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



### <span data-ttu-id="1895d-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="1895d-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="1895d-138">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="1895d-138">Private Container Registry Username</span></span>



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



### <span data-ttu-id="1895d-139">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="1895d-139">-DefaultDocuments</span></span>

<span data-ttu-id="1895d-140">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="1895d-140">Default Documents String Array</span></span>



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



### <span data-ttu-id="1895d-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1895d-141">-DefaultProfile</span></span>

<span data-ttu-id="1895d-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1895d-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



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



### <span data-ttu-id="1895d-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1895d-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="1895d-144">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="1895d-144">Detailed Error Logging Enabled Boolean</span></span>



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



### <span data-ttu-id="1895d-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="1895d-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="1895d-146">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="1895d-146">Enables/Disables container continuous deployment webhook</span></span>



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



### <span data-ttu-id="1895d-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="1895d-147">-HandlerMappings</span></span>

<span data-ttu-id="1895d-148">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="1895d-148">Handler Mappings IList</span></span>



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



### <span data-ttu-id="1895d-149">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="1895d-149">-HostNames</span></span>

<span data-ttu-id="1895d-150">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-150">WebApp HostNames String Array</span></span>



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



### <span data-ttu-id="1895d-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1895d-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="1895d-152">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="1895d-152">HttpLoggingEnabled Boolean</span></span>



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



### <span data-ttu-id="1895d-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1895d-153">-HttpsOnly</span></span>

<span data-ttu-id="1895d-154">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="1895d-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="1895d-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="1895d-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="1895d-156">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="1895d-156">Managed Pipeline Mode Name</span></span>



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



### <span data-ttu-id="1895d-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="1895d-157">-Name</span></span>

<span data-ttu-id="1895d-158">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-158">WebApp Name</span></span>



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



### <span data-ttu-id="1895d-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="1895d-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="1895d-160">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="1895d-160">Net Framework Version</span></span>



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



### <span data-ttu-id="1895d-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="1895d-161">-NumberOfWorkers</span></span>

<span data-ttu-id="1895d-162">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="1895d-162">The number of workers to be allocated</span></span>



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



### <span data-ttu-id="1895d-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="1895d-163">-PhpVersion</span></span>

<span data-ttu-id="1895d-164">Versão do php</span><span class="sxs-lookup"><span data-stu-id="1895d-164">Php Version</span></span>



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



### <span data-ttu-id="1895d-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="1895d-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="1895d-166">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="1895d-166">Request Tracing Enabled</span></span>



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



### <span data-ttu-id="1895d-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1895d-167">-ResourceGroupName</span></span>

<span data-ttu-id="1895d-168">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1895d-168">Resource Group Name</span></span>



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



### <span data-ttu-id="1895d-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="1895d-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="1895d-170">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="1895d-170">Use 32-bit Worker Process Boolean</span></span>



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



### <span data-ttu-id="1895d-171">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-171">-WebApp</span></span>

<span data-ttu-id="1895d-172">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-172">WebApp Object</span></span>



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



### <span data-ttu-id="1895d-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="1895d-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="1895d-174">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="1895d-174">WebSocketsEnabled Boolean</span></span>



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



### <span data-ttu-id="1895d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1895d-175">CommonParameters</span></span>

<span data-ttu-id="1895d-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1895d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1895d-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1895d-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="1895d-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1895d-178">INPUTS</span></span>



### <span data-ttu-id="1895d-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1895d-179">System.Int32</span></span>



### <span data-ttu-id="1895d-180">System. String</span><span class="sxs-lookup"><span data-stu-id="1895d-180">System.String</span></span>



### <span data-ttu-id="1895d-181">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1895d-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="1895d-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1895d-182">OUTPUTS</span></span>



### <span data-ttu-id="1895d-183">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1895d-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="1895d-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1895d-184">NOTES</span></span>



## <span data-ttu-id="1895d-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1895d-185">RELATED LINKS</span></span>



[<span data-ttu-id="1895d-186">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="1895d-187">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="1895d-188">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="1895d-189">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="1895d-190">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="1895d-191">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1895d-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

