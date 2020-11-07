---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945433"
---
# <span data-ttu-id="9c74c-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9c74c-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="9c74c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c74c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c74c-103">Configura um site em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="9c74c-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="9c74c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c74c-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c74c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c74c-105">DESCRIPTION</span></span>
<span data-ttu-id="9c74c-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9c74c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9c74c-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9c74c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9c74c-108">O cmdlet **set-AzureWebsite** configura um site em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="9c74c-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="9c74c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c74c-109">EXAMPLES</span></span>

### <span data-ttu-id="9c74c-110">Exemplo 1: habilitar o log HTTP para um site</span><span class="sxs-lookup"><span data-stu-id="9c74c-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="9c74c-111">Este exemplo ativa o log HTTP.</span><span class="sxs-lookup"><span data-stu-id="9c74c-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="9c74c-112">Exemplo 2: definir credenciais de armazenamento para um site</span><span class="sxs-lookup"><span data-stu-id="9c74c-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="9c74c-113">Este exemplo define as credenciais de armazenamento em um site denominado mywebsite com variáveis de ambiente para AZURE_STORAGE_ACCOUNT e AZURE_STORAGE_ACCESS_KEY.</span><span class="sxs-lookup"><span data-stu-id="9c74c-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="9c74c-114">OS</span><span class="sxs-lookup"><span data-stu-id="9c74c-114">PARAMETERS</span></span>

### <span data-ttu-id="9c74c-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="9c74c-115">-AppSettings</span></span>
<span data-ttu-id="9c74c-116">Especifica as variáveis de ambiente que serão usadas pelo website.</span><span class="sxs-lookup"><span data-stu-id="9c74c-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="9c74c-117">-AutoSwapSlotName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="9c74c-118">-ConnectionStrings</span></span>
<span data-ttu-id="9c74c-119">Especifica as cadeias de conexão usadas pelo website.</span><span class="sxs-lookup"><span data-stu-id="9c74c-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-120">-Defaultdocuments</span><span class="sxs-lookup"><span data-stu-id="9c74c-120">-DefaultDocuments</span></span>
<span data-ttu-id="9c74c-121">Especifica os documentos que são exibidos automaticamente ao navegar pelo site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9c74c-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="9c74c-123">Determina se erros do IIS detalhados são registrados para o site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="9c74c-124">-HandlerMappings</span></span>
<span data-ttu-id="9c74c-125">Especifica os mapeamentos de manipulador usados pelo website.</span><span class="sxs-lookup"><span data-stu-id="9c74c-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-126">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="9c74c-126">-HostNames</span></span>
<span data-ttu-id="9c74c-127">Especifica os nomes de host totalmente qualificados que podem ser usados para acessar o site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9c74c-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="9c74c-129">Determina se o log http está habilitado para o site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="9c74c-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="9c74c-131">Especifica o modo de pipeline gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9c74c-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-132">-Metadados</span><span class="sxs-lookup"><span data-stu-id="9c74c-132">-Metadata</span></span>
<span data-ttu-id="9c74c-133">Especifica os metadados do site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c74c-134">-Name</span></span>
<span data-ttu-id="9c74c-135">Especifica o nome do site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-135">Specifies the name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="9c74c-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="9c74c-137">Especifica a versão do .NET Framework exigida pelo website.</span><span class="sxs-lookup"><span data-stu-id="9c74c-137">Specifies the version of the .Net Framework required by the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="9c74c-138">-NumberOfWorkers</span></span>
<span data-ttu-id="9c74c-139">Especifica o número de processos de trabalho que executam o site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c74c-140">-PassThru</span></span>
<span data-ttu-id="9c74c-141">Indica que esse cmdlet retorna um valor **booliano** .</span><span class="sxs-lookup"><span data-stu-id="9c74c-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="9c74c-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="9c74c-142">-PhpVersion</span></span>
<span data-ttu-id="9c74c-143">Especifica a versão do PHP necessária para o site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-143">Specifies the PHP version required by the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-144">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9c74c-144">-Profile</span></span>
<span data-ttu-id="9c74c-145">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9c74c-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c74c-146">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9c74c-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="9c74c-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="9c74c-148">Determina se o rastreamento de solicitação está habilitado para o site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="9c74c-149">-RoutingRules</span></span>
<span data-ttu-id="9c74c-150">Especifica as regras de roteamento a serem usadas para testar em produção.</span><span class="sxs-lookup"><span data-stu-id="9c74c-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="9c74c-151">-SiteWithConfig</span></span>
<span data-ttu-id="9c74c-152">Especifica a configuração usada pelo website.</span><span class="sxs-lookup"><span data-stu-id="9c74c-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-153">-Slot</span><span class="sxs-lookup"><span data-stu-id="9c74c-153">-Slot</span></span>
<span data-ttu-id="9c74c-154">Especifica o nome do slot do site.</span><span class="sxs-lookup"><span data-stu-id="9c74c-154">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="9c74c-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="9c74c-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="9c74c-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="9c74c-158">Especifica se o modo de 32 bits deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="9c74c-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="9c74c-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="9c74c-160">Especifica se devem ser habilitados WebSockets.</span><span class="sxs-lookup"><span data-stu-id="9c74c-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c74c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c74c-161">CommonParameters</span></span>
<span data-ttu-id="9c74c-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c74c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c74c-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c74c-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c74c-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c74c-164">INPUTS</span></span>

## <span data-ttu-id="9c74c-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c74c-165">OUTPUTS</span></span>

## <span data-ttu-id="9c74c-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c74c-166">NOTES</span></span>

## <span data-ttu-id="9c74c-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c74c-167">RELATED LINKS</span></span>

[<span data-ttu-id="9c74c-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9c74c-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="9c74c-169">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9c74c-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="9c74c-170">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9c74c-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


