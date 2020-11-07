---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 245ce5ab011f03b8d8331b5d80fa4eeb01e19e15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786196"
---
# <span data-ttu-id="d99a7-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d99a7-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d99a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d99a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d99a7-103">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d99a7-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d99a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d99a7-104">SYNTAX</span></span>

### <span data-ttu-id="d99a7-105">Eles</span><span class="sxs-lookup"><span data-stu-id="d99a7-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d99a7-106">S2</span><span class="sxs-lookup"><span data-stu-id="d99a7-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d99a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d99a7-107">DESCRIPTION</span></span>
<span data-ttu-id="d99a7-108">O cmdlet **set-AzureRmWebApp** define um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d99a7-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="d99a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d99a7-109">EXAMPLES</span></span>

### <span data-ttu-id="d99a7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d99a7-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="d99a7-111">Esse comando define HttpLoggingEnabled como true para o slot Slot001 pertencentes ao ContosoWebApp do aplicativo Web associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="d99a7-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d99a7-112">OS</span><span class="sxs-lookup"><span data-stu-id="d99a7-112">PARAMETERS</span></span>

### <span data-ttu-id="d99a7-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d99a7-113">-AppServicePlan</span></span>
<span data-ttu-id="d99a7-114">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d99a7-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="d99a7-115">-AppSettings</span></span>
<span data-ttu-id="d99a7-116">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="d99a7-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="d99a7-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="d99a7-118">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="d99a7-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="d99a7-119">-ConnectionStrings</span></span>
<span data-ttu-id="d99a7-120">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="d99a7-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-121">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="d99a7-121">-DefaultDocuments</span></span>
<span data-ttu-id="d99a7-122">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="d99a7-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d99a7-123">-DefaultProfile</span></span>
<span data-ttu-id="d99a7-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d99a7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d99a7-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="d99a7-126">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="d99a7-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="d99a7-127">-HandlerMappings</span></span>
<span data-ttu-id="d99a7-128">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="d99a7-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="d99a7-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d99a7-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="d99a7-130">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="d99a7-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="d99a7-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="d99a7-132">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="d99a7-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="d99a7-133">-Name</span></span>
<span data-ttu-id="d99a7-134">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="d99a7-134">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="d99a7-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="d99a7-136">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d99a7-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="d99a7-137">-NumberOfWorkers</span></span>
<span data-ttu-id="d99a7-138">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="d99a7-138">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="d99a7-139">-PhpVersion</span></span>
<span data-ttu-id="d99a7-140">Versão do php</span><span class="sxs-lookup"><span data-stu-id="d99a7-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="d99a7-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="d99a7-142">Booleano de rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="d99a7-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d99a7-143">-ResourceGroupName</span></span>
<span data-ttu-id="d99a7-144">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d99a7-144">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="d99a7-145">-Slot</span></span>
<span data-ttu-id="d99a7-146">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="d99a7-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="d99a7-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="d99a7-148">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d99a7-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d99a7-149">-WebApp</span></span>
<span data-ttu-id="d99a7-150">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="d99a7-150">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d99a7-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="d99a7-152">Booleano habilitados para Web Sockets</span><span class="sxs-lookup"><span data-stu-id="d99a7-152">Web Sockets Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="d99a7-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d99a7-153">-HttpsOnly</span></span>
<span data-ttu-id="d99a7-154">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um slot existente</span><span class="sxs-lookup"><span data-stu-id="d99a7-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="d99a7-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d99a7-155">-AssignIdentity</span></span>
<span data-ttu-id="d99a7-156">Habilitar/desabilitar o MSI em um slot existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="d99a7-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d99a7-157">-AsJob</span></span>
<span data-ttu-id="d99a7-158">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d99a7-158">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d99a7-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99a7-159">CommonParameters</span></span>
<span data-ttu-id="d99a7-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d99a7-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99a7-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d99a7-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99a7-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d99a7-162">INPUTS</span></span>

### <span data-ttu-id="d99a7-163">Int32</span><span class="sxs-lookup"><span data-stu-id="d99a7-163">Int32</span></span>
<span data-ttu-id="d99a7-164">O parâmetro ' NumberOfWorkers ' aceita o valor do tipo ' Int32 ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d99a7-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="d99a7-165">Instalação</span><span class="sxs-lookup"><span data-stu-id="d99a7-165">Site</span></span>
<span data-ttu-id="d99a7-166">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="d99a7-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d99a7-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d99a7-167">OUTPUTS</span></span>

## <span data-ttu-id="d99a7-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d99a7-168">NOTES</span></span>

## <span data-ttu-id="d99a7-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d99a7-169">RELATED LINKS</span></span>

[<span data-ttu-id="d99a7-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d99a7-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="d99a7-171">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d99a7-171">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="d99a7-172">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d99a7-172">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="d99a7-173">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d99a7-173">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="d99a7-174">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d99a7-174">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="d99a7-175">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d99a7-175">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="d99a7-176">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d99a7-176">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
