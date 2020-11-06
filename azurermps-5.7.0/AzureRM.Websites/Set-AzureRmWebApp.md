---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433351"
---
# <span data-ttu-id="206fc-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="206fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="206fc-102">SYNOPSIS</span></span>
<span data-ttu-id="206fc-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="206fc-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="206fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="206fc-104">SYNTAX</span></span>

### <span data-ttu-id="206fc-105">Eles</span><span class="sxs-lookup"><span data-stu-id="206fc-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="206fc-106">S2</span><span class="sxs-lookup"><span data-stu-id="206fc-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="206fc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="206fc-107">DESCRIPTION</span></span>
<span data-ttu-id="206fc-108">O cmdlet **set-AzureRmWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="206fc-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="206fc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="206fc-109">EXAMPLES</span></span>

### <span data-ttu-id="206fc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="206fc-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="206fc-111">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="206fc-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="206fc-112">OS</span><span class="sxs-lookup"><span data-stu-id="206fc-112">PARAMETERS</span></span>

### <span data-ttu-id="206fc-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="206fc-113">-AppServicePlan</span></span>
<span data-ttu-id="206fc-114">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="206fc-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="206fc-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="206fc-115">-AppSettings</span></span>
<span data-ttu-id="206fc-116">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="206fc-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="206fc-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="206fc-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="206fc-118">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="206fc-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="206fc-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="206fc-119">-ConnectionStrings</span></span>
<span data-ttu-id="206fc-120">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="206fc-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="206fc-121">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="206fc-121">-DefaultDocuments</span></span>
<span data-ttu-id="206fc-122">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="206fc-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="206fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206fc-123">-DefaultProfile</span></span>
<span data-ttu-id="206fc-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="206fc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="206fc-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="206fc-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="206fc-126">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="206fc-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="206fc-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="206fc-127">-HandlerMappings</span></span>
<span data-ttu-id="206fc-128">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="206fc-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="206fc-129">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="206fc-129">-HostNames</span></span>
<span data-ttu-id="206fc-130">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-130">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="206fc-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="206fc-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="206fc-132">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="206fc-132">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="206fc-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="206fc-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="206fc-134">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="206fc-134">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="206fc-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="206fc-135">-Name</span></span>
<span data-ttu-id="206fc-136">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-136">WebApp Name</span></span>

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

### <span data-ttu-id="206fc-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="206fc-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="206fc-138">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="206fc-138">Net Framework Version</span></span>

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

### <span data-ttu-id="206fc-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="206fc-139">-NumberOfWorkers</span></span>
<span data-ttu-id="206fc-140">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="206fc-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="206fc-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="206fc-141">-PhpVersion</span></span>
<span data-ttu-id="206fc-142">Versão do php</span><span class="sxs-lookup"><span data-stu-id="206fc-142">Php Version</span></span>

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

### <span data-ttu-id="206fc-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="206fc-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="206fc-144">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="206fc-144">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="206fc-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206fc-145">-ResourceGroupName</span></span>
<span data-ttu-id="206fc-146">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="206fc-146">Resource Group Name</span></span>

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

### <span data-ttu-id="206fc-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="206fc-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="206fc-148">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="206fc-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="206fc-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-149">-WebApp</span></span>
<span data-ttu-id="206fc-150">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-150">WebApp Object</span></span>

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

### <span data-ttu-id="206fc-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="206fc-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="206fc-152">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="206fc-152">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="206fc-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="206fc-153">-AsJob</span></span>
<span data-ttu-id="206fc-154">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="206fc-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="206fc-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206fc-155">CommonParameters</span></span>
<span data-ttu-id="206fc-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="206fc-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="206fc-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="206fc-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206fc-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="206fc-158">INPUTS</span></span>

### <span data-ttu-id="206fc-159">Int32</span><span class="sxs-lookup"><span data-stu-id="206fc-159">Int32</span></span>
<span data-ttu-id="206fc-160">O parâmetro ' NumberOfWorkers ' aceita o valor do tipo ' Int32 ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="206fc-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="206fc-161">Instalação</span><span class="sxs-lookup"><span data-stu-id="206fc-161">Site</span></span>
<span data-ttu-id="206fc-162">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="206fc-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="206fc-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="206fc-163">OUTPUTS</span></span>

## <span data-ttu-id="206fc-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="206fc-164">NOTES</span></span>

## <span data-ttu-id="206fc-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="206fc-165">RELATED LINKS</span></span>

[<span data-ttu-id="206fc-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="206fc-167">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="206fc-168">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="206fc-169">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="206fc-170">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="206fc-171">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="206fc-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
