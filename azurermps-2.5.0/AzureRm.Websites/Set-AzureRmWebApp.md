---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: d722c378e246fa175741c91092d99415275f094e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785584"
---
# <span data-ttu-id="2281e-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="2281e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2281e-102">SYNOPSIS</span></span>
<span data-ttu-id="2281e-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="2281e-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2281e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2281e-104">SYNTAX</span></span>

### <span data-ttu-id="2281e-105">Eles</span><span class="sxs-lookup"><span data-stu-id="2281e-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2281e-106">S2</span><span class="sxs-lookup"><span data-stu-id="2281e-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2281e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2281e-107">DESCRIPTION</span></span>
<span data-ttu-id="2281e-108">O cmdlet **set-AzureRmWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="2281e-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="2281e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2281e-109">EXAMPLES</span></span>

### <span data-ttu-id="2281e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2281e-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="2281e-111">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="2281e-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2281e-112">OS</span><span class="sxs-lookup"><span data-stu-id="2281e-112">PARAMETERS</span></span>

### <span data-ttu-id="2281e-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2281e-113">-AppServicePlan</span></span>
<span data-ttu-id="2281e-114">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2281e-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="2281e-115">-AppSettings</span></span>
<span data-ttu-id="2281e-116">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2281e-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2281e-117">-AsJob</span></span>
<span data-ttu-id="2281e-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2281e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2281e-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2281e-119">-AssignIdentity</span></span>
<span data-ttu-id="2281e-120">Habilitar/desabilitar o MSI em um webapp ou functionapp do Azure existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="2281e-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

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

### <span data-ttu-id="2281e-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="2281e-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="2281e-122">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="2281e-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="2281e-123">-ConnectionStrings</span></span>
<span data-ttu-id="2281e-124">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="2281e-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-125">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="2281e-125">-DefaultDocuments</span></span>
<span data-ttu-id="2281e-126">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="2281e-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2281e-127">-DefaultProfile</span></span>
<span data-ttu-id="2281e-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2281e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2281e-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2281e-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="2281e-130">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="2281e-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="2281e-131">-HandlerMappings</span></span>
<span data-ttu-id="2281e-132">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="2281e-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="2281e-133">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="2281e-133">-HostNames</span></span>
<span data-ttu-id="2281e-134">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2281e-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="2281e-136">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="2281e-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2281e-137">-HttpsOnly</span></span>
<span data-ttu-id="2281e-138">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="2281e-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="2281e-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="2281e-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="2281e-140">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="2281e-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="2281e-141">-Name</span></span>
<span data-ttu-id="2281e-142">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-142">WebApp Name</span></span>

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

### <span data-ttu-id="2281e-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="2281e-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="2281e-144">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2281e-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="2281e-145">-NumberOfWorkers</span></span>
<span data-ttu-id="2281e-146">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="2281e-146">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="2281e-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="2281e-147">-PhpVersion</span></span>
<span data-ttu-id="2281e-148">Versão do php</span><span class="sxs-lookup"><span data-stu-id="2281e-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="2281e-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="2281e-150">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="2281e-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2281e-151">-ResourceGroupName</span></span>
<span data-ttu-id="2281e-152">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2281e-152">Resource Group Name</span></span>

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

### <span data-ttu-id="2281e-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="2281e-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="2281e-154">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="2281e-154">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="2281e-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-155">-WebApp</span></span>
<span data-ttu-id="2281e-156">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-156">WebApp Object</span></span>

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

### <span data-ttu-id="2281e-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="2281e-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="2281e-158">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="2281e-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2281e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2281e-159">CommonParameters</span></span>
<span data-ttu-id="2281e-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2281e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2281e-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2281e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2281e-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2281e-162">INPUTS</span></span>

### <span data-ttu-id="2281e-163">Int32</span><span class="sxs-lookup"><span data-stu-id="2281e-163">Int32</span></span>
<span data-ttu-id="2281e-164">O parâmetro ' NumberOfWorkers ' aceita o valor do tipo ' Int32 ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2281e-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="2281e-165">Instalação</span><span class="sxs-lookup"><span data-stu-id="2281e-165">Site</span></span>
<span data-ttu-id="2281e-166">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="2281e-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2281e-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2281e-167">OUTPUTS</span></span>

## <span data-ttu-id="2281e-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2281e-168">NOTES</span></span>

## <span data-ttu-id="2281e-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2281e-169">RELATED LINKS</span></span>

[<span data-ttu-id="2281e-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="2281e-171">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-171">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="2281e-172">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-172">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="2281e-173">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-173">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="2281e-174">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-174">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="2281e-175">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2281e-175">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
