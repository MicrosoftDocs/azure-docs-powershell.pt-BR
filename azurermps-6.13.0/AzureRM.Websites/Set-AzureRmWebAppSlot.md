---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430769"
---
# <span data-ttu-id="094f2-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094f2-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="094f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="094f2-102">SYNOPSIS</span></span>
<span data-ttu-id="094f2-103">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="094f2-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="094f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="094f2-104">SYNTAX</span></span>

### <span data-ttu-id="094f2-105">Eles</span><span class="sxs-lookup"><span data-stu-id="094f2-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="094f2-106">S2</span><span class="sxs-lookup"><span data-stu-id="094f2-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="094f2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="094f2-107">DESCRIPTION</span></span>
<span data-ttu-id="094f2-108">O cmdlet **set-AzureRmWebApp** define um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="094f2-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="094f2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="094f2-109">EXAMPLES</span></span>

### <span data-ttu-id="094f2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="094f2-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="094f2-111">Esse comando define HttpLoggingEnabled como true para o slot Slot001 pertencentes ao ContosoWebApp do aplicativo Web associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="094f2-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="094f2-112">OS</span><span class="sxs-lookup"><span data-stu-id="094f2-112">PARAMETERS</span></span>

### <span data-ttu-id="094f2-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="094f2-113">-AppServicePlan</span></span>
<span data-ttu-id="094f2-114">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="094f2-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="094f2-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="094f2-115">-AppSettings</span></span>
<span data-ttu-id="094f2-116">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="094f2-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="094f2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="094f2-117">-AsJob</span></span>
<span data-ttu-id="094f2-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="094f2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="094f2-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="094f2-119">-AssignIdentity</span></span>
<span data-ttu-id="094f2-120">Habilitar/desabilitar o MSI em um slot existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="094f2-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="094f2-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="094f2-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="094f2-122">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="094f2-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="094f2-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="094f2-123">-ConnectionStrings</span></span>
<span data-ttu-id="094f2-124">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="094f2-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="094f2-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="094f2-125">-ContainerImageName</span></span>
<span data-ttu-id="094f2-126">Nome da imagem do contêiner</span><span class="sxs-lookup"><span data-stu-id="094f2-126">Container Image Name</span></span>

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

### <span data-ttu-id="094f2-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="094f2-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="094f2-128">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="094f2-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="094f2-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="094f2-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="094f2-130">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="094f2-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="094f2-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="094f2-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="094f2-132">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="094f2-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="094f2-133">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="094f2-133">-DefaultDocuments</span></span>
<span data-ttu-id="094f2-134">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="094f2-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="094f2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094f2-135">-DefaultProfile</span></span>
<span data-ttu-id="094f2-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="094f2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="094f2-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="094f2-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="094f2-138">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="094f2-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="094f2-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="094f2-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="094f2-140">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="094f2-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="094f2-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="094f2-141">-HandlerMappings</span></span>
<span data-ttu-id="094f2-142">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="094f2-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="094f2-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="094f2-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="094f2-144">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="094f2-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="094f2-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="094f2-145">-HttpsOnly</span></span>
<span data-ttu-id="094f2-146">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um slot existente</span><span class="sxs-lookup"><span data-stu-id="094f2-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="094f2-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="094f2-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="094f2-148">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="094f2-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="094f2-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="094f2-149">-Name</span></span>
<span data-ttu-id="094f2-150">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="094f2-150">WebApp Name</span></span>

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

### <span data-ttu-id="094f2-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="094f2-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="094f2-152">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="094f2-152">Net Framework Version</span></span>

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

### <span data-ttu-id="094f2-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="094f2-153">-NumberOfWorkers</span></span>
<span data-ttu-id="094f2-154">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="094f2-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="094f2-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="094f2-155">-PhpVersion</span></span>
<span data-ttu-id="094f2-156">Versão do php</span><span class="sxs-lookup"><span data-stu-id="094f2-156">Php Version</span></span>

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

### <span data-ttu-id="094f2-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="094f2-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="094f2-158">Booleano de rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="094f2-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="094f2-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094f2-159">-ResourceGroupName</span></span>
<span data-ttu-id="094f2-160">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="094f2-160">Resource Group Name</span></span>

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

### <span data-ttu-id="094f2-161">-Slot</span><span class="sxs-lookup"><span data-stu-id="094f2-161">-Slot</span></span>
<span data-ttu-id="094f2-162">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="094f2-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="094f2-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="094f2-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="094f2-164">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="094f2-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="094f2-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="094f2-165">-WebApp</span></span>
<span data-ttu-id="094f2-166">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="094f2-166">WebApp Object</span></span>

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

### <span data-ttu-id="094f2-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="094f2-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="094f2-168">Booleano habilitados para Web Sockets</span><span class="sxs-lookup"><span data-stu-id="094f2-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="094f2-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094f2-169">CommonParameters</span></span>
<span data-ttu-id="094f2-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="094f2-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094f2-171">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="094f2-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094f2-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="094f2-172">INPUTS</span></span>

### <span data-ttu-id="094f2-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="094f2-173">System.Int32</span></span>
<span data-ttu-id="094f2-174">Parâmetros: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="094f2-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="094f2-175">System. String</span><span class="sxs-lookup"><span data-stu-id="094f2-175">System.String</span></span>

### <span data-ttu-id="094f2-176">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="094f2-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="094f2-177">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="094f2-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="094f2-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="094f2-178">OUTPUTS</span></span>

### <span data-ttu-id="094f2-179">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="094f2-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="094f2-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="094f2-180">NOTES</span></span>

## <span data-ttu-id="094f2-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="094f2-181">RELATED LINKS</span></span>

[<span data-ttu-id="094f2-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094f2-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="094f2-183">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094f2-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="094f2-184">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094f2-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="094f2-185">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094f2-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="094f2-186">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094f2-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="094f2-187">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094f2-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="094f2-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="094f2-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
