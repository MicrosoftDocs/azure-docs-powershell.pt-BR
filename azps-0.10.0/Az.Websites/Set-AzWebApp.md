---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4478083a2ee98eceda08012b4346f3ece1657963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776062"
---
# <span data-ttu-id="3ffb8-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-101">Set-AzWebApp</span></span>

## <span data-ttu-id="3ffb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ffb8-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffb8-103">Modifica um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ffb8-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="3ffb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ffb8-104">SYNTAX</span></span>

### <span data-ttu-id="3ffb8-105">Eles</span><span class="sxs-lookup"><span data-stu-id="3ffb8-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ffb8-106">S2</span><span class="sxs-lookup"><span data-stu-id="3ffb8-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ffb8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ffb8-107">DESCRIPTION</span></span>
<span data-ttu-id="3ffb8-108">O cmdlet **set-AzWebApp** define um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ffb8-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="3ffb8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ffb8-109">EXAMPLES</span></span>

### <span data-ttu-id="3ffb8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ffb8-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="3ffb8-111">Esse comando define HttpLoggingEnabled como true para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="3ffb8-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3ffb8-112">OS</span><span class="sxs-lookup"><span data-stu-id="3ffb8-112">PARAMETERS</span></span>

### <span data-ttu-id="3ffb8-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ffb8-113">-AppServicePlan</span></span>
<span data-ttu-id="3ffb8-114">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="3ffb8-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="3ffb8-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="3ffb8-115">-AppSettings</span></span>
<span data-ttu-id="3ffb8-116">HashTable das configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="3ffb8-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="3ffb8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ffb8-117">-AsJob</span></span>
<span data-ttu-id="3ffb8-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3ffb8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ffb8-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3ffb8-119">-AssignIdentity</span></span>
<span data-ttu-id="3ffb8-120">Habilitar/desabilitar o MSI em um webapp ou functionapp do Azure existente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="3ffb8-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

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

### <span data-ttu-id="3ffb8-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="3ffb8-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="3ffb8-122">Nome do slot de destino para troca automática</span><span class="sxs-lookup"><span data-stu-id="3ffb8-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="3ffb8-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="3ffb8-123">-ConnectionStrings</span></span>
<span data-ttu-id="3ffb8-124">HashTable da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="3ffb8-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="3ffb8-125">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="3ffb8-125">-DefaultDocuments</span></span>
<span data-ttu-id="3ffb8-126">Matriz de cadeia de caracteres de documentos padrão</span><span class="sxs-lookup"><span data-stu-id="3ffb8-126">Default Documents String Array</span></span>

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

### <span data-ttu-id="3ffb8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffb8-127">-DefaultProfile</span></span>
<span data-ttu-id="3ffb8-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ffb8-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ffb8-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3ffb8-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="3ffb8-130">Booliano detalhado de log de erros ativado</span><span class="sxs-lookup"><span data-stu-id="3ffb8-130">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="3ffb8-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="3ffb8-131">-HandlerMappings</span></span>
<span data-ttu-id="3ffb8-132">Mapeamentos de manipuladores IList</span><span class="sxs-lookup"><span data-stu-id="3ffb8-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="3ffb8-133">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="3ffb8-133">-HostNames</span></span>
<span data-ttu-id="3ffb8-134">Matriz de cadeia de caracteres de hosts WebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-134">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="3ffb8-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3ffb8-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="3ffb8-136">HttpLoggingEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="3ffb8-136">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="3ffb8-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3ffb8-137">-HttpsOnly</span></span>
<span data-ttu-id="3ffb8-138">Habilitar/desabilitar o redirecionamento de todo o tráfego para HTTPS em um Azure webapp ou functionapp existente</span><span class="sxs-lookup"><span data-stu-id="3ffb8-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="3ffb8-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="3ffb8-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="3ffb8-140">Nome do modo de pipeline gerenciado</span><span class="sxs-lookup"><span data-stu-id="3ffb8-140">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="3ffb8-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ffb8-141">-Name</span></span>
<span data-ttu-id="3ffb8-142">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-142">WebApp Name</span></span>

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

### <span data-ttu-id="3ffb8-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="3ffb8-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="3ffb8-144">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="3ffb8-144">Net Framework Version</span></span>

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

### <span data-ttu-id="3ffb8-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="3ffb8-145">-NumberOfWorkers</span></span>
<span data-ttu-id="3ffb8-146">O número de trabalhadores a serem atribuídos</span><span class="sxs-lookup"><span data-stu-id="3ffb8-146">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="3ffb8-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="3ffb8-147">-PhpVersion</span></span>
<span data-ttu-id="3ffb8-148">Versão do php</span><span class="sxs-lookup"><span data-stu-id="3ffb8-148">Php Version</span></span>

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

### <span data-ttu-id="3ffb8-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="3ffb8-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="3ffb8-150">Rastreamento de solicitação habilitado</span><span class="sxs-lookup"><span data-stu-id="3ffb8-150">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="3ffb8-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ffb8-151">-ResourceGroupName</span></span>
<span data-ttu-id="3ffb8-152">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3ffb8-152">Resource Group Name</span></span>

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

### <span data-ttu-id="3ffb8-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="3ffb8-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="3ffb8-154">Usar booliano do processo de trabalho de 32 bits</span><span class="sxs-lookup"><span data-stu-id="3ffb8-154">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="3ffb8-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-155">-WebApp</span></span>
<span data-ttu-id="3ffb8-156">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-156">WebApp Object</span></span>

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

### <span data-ttu-id="3ffb8-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="3ffb8-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="3ffb8-158">WebSocketsEnabled booliano</span><span class="sxs-lookup"><span data-stu-id="3ffb8-158">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="3ffb8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffb8-159">CommonParameters</span></span>
<span data-ttu-id="3ffb8-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ffb8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffb8-161">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ffb8-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffb8-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ffb8-162">INPUTS</span></span>

### <span data-ttu-id="3ffb8-163">Int32</span><span class="sxs-lookup"><span data-stu-id="3ffb8-163">Int32</span></span>
<span data-ttu-id="3ffb8-164">O parâmetro ' NumberOfWorkers ' aceita o valor do tipo ' Int32 ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3ffb8-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="3ffb8-165">Instalação</span><span class="sxs-lookup"><span data-stu-id="3ffb8-165">Site</span></span>
<span data-ttu-id="3ffb8-166">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="3ffb8-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3ffb8-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ffb8-167">OUTPUTS</span></span>

## <span data-ttu-id="3ffb8-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ffb8-168">NOTES</span></span>

## <span data-ttu-id="3ffb8-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ffb8-169">RELATED LINKS</span></span>

[<span data-ttu-id="3ffb8-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3ffb8-171">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-171">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3ffb8-172">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-172">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3ffb8-173">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-173">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3ffb8-174">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-174">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="3ffb8-175">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3ffb8-175">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
