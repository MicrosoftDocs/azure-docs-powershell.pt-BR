---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: b6cb41e49695fa7fd9fa0efdefdbefb2b23229a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776061"
---
# <span data-ttu-id="3a938-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a938-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="3a938-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a938-102">SYNOPSIS</span></span>
<span data-ttu-id="3a938-103">Modifica um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3a938-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="3a938-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a938-104">SYNTAX</span></span>

### <span data-ttu-id="3a938-105">Eles</span><span class="sxs-lookup"><span data-stu-id="3a938-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a938-106">S2</span><span class="sxs-lookup"><span data-stu-id="3a938-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a938-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a938-107">DESCRIPTION</span></span>
<span data-ttu-id="3a938-108">O cmdlet **set-AzWebApp** define um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3a938-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="3a938-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a938-109">EXAMPLES</span></span>

### <span data-ttu-id="3a938-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a938-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="3a938-111">Esse comando define HttpLoggingEnabled como true para o slot Slot001 pertencentes ao ContosoWebApp do aplicativo Web associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="3a938-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3a938-112">OS</span><span class="sxs-lookup"><span data-stu-id="3a938-112">PARAMETERS</span></span>

### <span data-ttu-id="3a938-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3a938-113">-AppServicePlan</span></span>
<span data-ttu-id="3a938-114">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="3a938-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="3a938-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="3a938-115">-AppSettings</span></span>
<span data-ttu-id="3a938-116">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="3a938-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="3a938-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="3a938-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="3a938-118">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="3a938-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="3a938-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="3a938-119">-ConnectionStrings</span></span>
<span data-ttu-id="3a938-120">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="3a938-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="3a938-121">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="3a938-121">-DefaultDocuments</span></span>
<span data-ttu-id="3a938-122">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="3a938-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="3a938-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a938-123">-DefaultProfile</span></span>
<span data-ttu-id="3a938-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a938-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a938-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3a938-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="3a938-126">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="3a938-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="3a938-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="3a938-127">-HandlerMappings</span></span>
<span data-ttu-id="3a938-128">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="3a938-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="3a938-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3a938-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="3a938-130">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="3a938-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="3a938-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="3a938-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="3a938-132">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="3a938-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="3a938-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a938-133">-Name</span></span>
<span data-ttu-id="3a938-134">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="3a938-134">WebApp Name</span></span>

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

### <span data-ttu-id="3a938-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="3a938-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="3a938-136">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="3a938-136">Net Framework Version</span></span>

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

### <span data-ttu-id="3a938-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="3a938-137">-NumberOfWorkers</span></span>
<span data-ttu-id="3a938-138">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="3a938-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="3a938-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="3a938-139">-PhpVersion</span></span>
<span data-ttu-id="3a938-140">Versão do php</span><span class="sxs-lookup"><span data-stu-id="3a938-140">Php Version</span></span>

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

### <span data-ttu-id="3a938-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="3a938-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="3a938-142">Booleano de rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="3a938-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="3a938-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a938-143">-ResourceGroupName</span></span>
<span data-ttu-id="3a938-144">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3a938-144">Resource Group Name</span></span>

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

### <span data-ttu-id="3a938-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="3a938-145">-Slot</span></span>
<span data-ttu-id="3a938-146">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="3a938-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3a938-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="3a938-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="3a938-148">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="3a938-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="3a938-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3a938-149">-WebApp</span></span>
<span data-ttu-id="3a938-150">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="3a938-150">WebApp Object</span></span>

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

### <span data-ttu-id="3a938-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="3a938-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="3a938-152">Booleano habilitados para Web Sockets</span><span class="sxs-lookup"><span data-stu-id="3a938-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="3a938-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3a938-153">-HttpsOnly</span></span>
<span data-ttu-id="3a938-154">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um slot existente</span><span class="sxs-lookup"><span data-stu-id="3a938-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="3a938-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3a938-155">-AssignIdentity</span></span>
<span data-ttu-id="3a938-156">Habilitar/desabilitar o MSI em um slot existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="3a938-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="3a938-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a938-157">-AsJob</span></span>
<span data-ttu-id="3a938-158">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3a938-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a938-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a938-159">CommonParameters</span></span>
<span data-ttu-id="3a938-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a938-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a938-161">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a938-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a938-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a938-162">INPUTS</span></span>

### <span data-ttu-id="3a938-163">Int32</span><span class="sxs-lookup"><span data-stu-id="3a938-163">Int32</span></span>
<span data-ttu-id="3a938-164">O parâmetro ' NumberOfWorkers ' aceita o valor do tipo ' Int32 ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3a938-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="3a938-165">Instalação</span><span class="sxs-lookup"><span data-stu-id="3a938-165">Site</span></span>
<span data-ttu-id="3a938-166">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="3a938-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3a938-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a938-167">OUTPUTS</span></span>

## <span data-ttu-id="3a938-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a938-168">NOTES</span></span>

## <span data-ttu-id="3a938-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a938-169">RELATED LINKS</span></span>

[<span data-ttu-id="3a938-170">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a938-170">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="3a938-171">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a938-171">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="3a938-172">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a938-172">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="3a938-173">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a938-173">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="3a938-174">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a938-174">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="3a938-175">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a938-175">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="3a938-176">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3a938-176">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
