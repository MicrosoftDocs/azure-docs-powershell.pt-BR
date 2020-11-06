---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428228"
---
# <span data-ttu-id="45b12-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="45b12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45b12-102">SYNOPSIS</span></span>
<span data-ttu-id="45b12-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="45b12-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45b12-104">SYNTAX</span></span>

### <span data-ttu-id="45b12-105">Eles</span><span class="sxs-lookup"><span data-stu-id="45b12-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45b12-106">S2</span><span class="sxs-lookup"><span data-stu-id="45b12-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b12-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45b12-107">DESCRIPTION</span></span>
<span data-ttu-id="45b12-108">O cmdlet **set-AzureRmWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="45b12-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="45b12-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45b12-109">EXAMPLES</span></span>

### <span data-ttu-id="45b12-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45b12-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="45b12-111">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="45b12-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="45b12-112">OS</span><span class="sxs-lookup"><span data-stu-id="45b12-112">PARAMETERS</span></span>

### <span data-ttu-id="45b12-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="45b12-113">-AppServicePlan</span></span>
<span data-ttu-id="45b12-114">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="45b12-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="45b12-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="45b12-115">-AppSettings</span></span>
<span data-ttu-id="45b12-116">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="45b12-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="45b12-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="45b12-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="45b12-118">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="45b12-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="45b12-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="45b12-119">-ConnectionStrings</span></span>
<span data-ttu-id="45b12-120">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="45b12-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="45b12-121">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="45b12-121">-DefaultDocuments</span></span>
<span data-ttu-id="45b12-122">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="45b12-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="45b12-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="45b12-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="45b12-124">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="45b12-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="45b12-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="45b12-125">-HandlerMappings</span></span>
<span data-ttu-id="45b12-126">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="45b12-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="45b12-127">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="45b12-127">-HostNames</span></span>
<span data-ttu-id="45b12-128">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-128">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="45b12-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="45b12-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="45b12-130">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="45b12-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="45b12-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="45b12-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="45b12-132">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="45b12-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="45b12-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="45b12-133">-Name</span></span>
<span data-ttu-id="45b12-134">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-134">WebApp Name</span></span>

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

### <span data-ttu-id="45b12-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="45b12-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="45b12-136">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="45b12-136">Net Framework Version</span></span>

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

### <span data-ttu-id="45b12-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="45b12-137">-NumberOfWorkers</span></span>
<span data-ttu-id="45b12-138">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="45b12-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="45b12-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="45b12-139">-PhpVersion</span></span>
<span data-ttu-id="45b12-140">Versão do php</span><span class="sxs-lookup"><span data-stu-id="45b12-140">Php Version</span></span>

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

### <span data-ttu-id="45b12-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="45b12-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="45b12-142">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="45b12-142">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="45b12-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b12-143">-ResourceGroupName</span></span>
<span data-ttu-id="45b12-144">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="45b12-144">Resource Group Name</span></span>

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

### <span data-ttu-id="45b12-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="45b12-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="45b12-146">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="45b12-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="45b12-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-147">-WebApp</span></span>
<span data-ttu-id="45b12-148">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45b12-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="45b12-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="45b12-150">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="45b12-150">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="45b12-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b12-151">-DefaultProfile</span></span>
<span data-ttu-id="45b12-152">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45b12-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b12-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b12-153">CommonParameters</span></span>
<span data-ttu-id="45b12-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b12-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b12-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b12-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b12-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45b12-156">INPUTS</span></span>

### <span data-ttu-id="45b12-157">Int32</span><span class="sxs-lookup"><span data-stu-id="45b12-157">Int32</span></span>
<span data-ttu-id="45b12-158">O parâmetro ' NumberOfWorkers ' aceita o valor do tipo ' Int32 ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="45b12-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="45b12-159">Instalação</span><span class="sxs-lookup"><span data-stu-id="45b12-159">Site</span></span>
<span data-ttu-id="45b12-160">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="45b12-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="45b12-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45b12-161">OUTPUTS</span></span>

## <span data-ttu-id="45b12-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45b12-162">NOTES</span></span>

## <span data-ttu-id="45b12-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45b12-163">RELATED LINKS</span></span>

[<span data-ttu-id="45b12-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="45b12-165">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="45b12-166">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="45b12-167">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="45b12-168">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="45b12-169">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45b12-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
