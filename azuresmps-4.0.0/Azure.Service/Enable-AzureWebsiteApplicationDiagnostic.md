---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945682"
---
# <span data-ttu-id="8f54f-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8f54f-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="8f54f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f54f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f54f-103">Habilita o diagnóstico de aplicativos em um site do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f54f-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="8f54f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f54f-104">SYNTAX</span></span>

### <span data-ttu-id="8f54f-105">Fileparameterset</span><span class="sxs-lookup"><span data-stu-id="8f54f-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8f54f-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f54f-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8f54f-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f54f-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f54f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f54f-108">DESCRIPTION</span></span>
<span data-ttu-id="8f54f-109">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8f54f-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8f54f-110">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8f54f-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8f54f-111">Habilita o diagnóstico de aplicativos em um site do Azure e permite que você configure o armazenamento de logs em um sistema de arquivos ou no armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f54f-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="8f54f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f54f-112">EXAMPLES</span></span>

### <span data-ttu-id="8f54f-113">Exemplo 1: habilitar diagnósticos usando o sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="8f54f-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="8f54f-114">Este exemplo habilita o log de aplicativo no sistema de arquivos com nível Verbose.</span><span class="sxs-lookup"><span data-stu-id="8f54f-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="8f54f-115">Exemplo 2: habilitar o registro em log usando o Azure Storage</span><span class="sxs-lookup"><span data-stu-id="8f54f-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="8f54f-116">Este exemplo habilita o log de aplicativos usando a conta de armazenamento chamada myaccount com nível de log definido para informações.</span><span class="sxs-lookup"><span data-stu-id="8f54f-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="8f54f-117">OS</span><span class="sxs-lookup"><span data-stu-id="8f54f-117">PARAMETERS</span></span>

### <span data-ttu-id="8f54f-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="8f54f-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f54f-119">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="8f54f-119">-File</span></span>
<span data-ttu-id="8f54f-120">Especifica que você deseja usar um sistema de arquivos para armazenar os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8f54f-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f54f-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="8f54f-121">-LogLevel</span></span>
<span data-ttu-id="8f54f-122">O nível de log para armazenar.</span><span class="sxs-lookup"><span data-stu-id="8f54f-122">The log level to store.</span></span>
<span data-ttu-id="8f54f-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8f54f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f54f-124">Erros</span><span class="sxs-lookup"><span data-stu-id="8f54f-124">Error</span></span>
- <span data-ttu-id="8f54f-125">Avisa</span><span class="sxs-lookup"><span data-stu-id="8f54f-125">Warning</span></span>
- <span data-ttu-id="8f54f-126">Às</span><span class="sxs-lookup"><span data-stu-id="8f54f-126">Information</span></span>
- <span data-ttu-id="8f54f-127">Detalha</span><span class="sxs-lookup"><span data-stu-id="8f54f-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f54f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f54f-128">-Name</span></span>
<span data-ttu-id="8f54f-129">Especifica o nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f54f-129">Specifies the name of the Azure website.</span></span>

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

### <span data-ttu-id="8f54f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f54f-130">-PassThru</span></span>
<span data-ttu-id="8f54f-131">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8f54f-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8f54f-132">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8f54f-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8f54f-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8f54f-133">-Profile</span></span>
<span data-ttu-id="8f54f-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8f54f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f54f-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8f54f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f54f-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="8f54f-136">-Slot</span></span>
<span data-ttu-id="8f54f-137">Especifica o nome do slot.</span><span class="sxs-lookup"><span data-stu-id="8f54f-137">Specifies the name of the slot.</span></span>

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

### <span data-ttu-id="8f54f-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8f54f-138">-StorageAccountName</span></span>
<span data-ttu-id="8f54f-139">A conta de armazenamento a ser usada para armazenar os logs.</span><span class="sxs-lookup"><span data-stu-id="8f54f-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="8f54f-140">Se não for especificado, o CurrentStorageAccount será usado.</span><span class="sxs-lookup"><span data-stu-id="8f54f-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f54f-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="8f54f-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f54f-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="8f54f-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f54f-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="8f54f-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f54f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f54f-144">CommonParameters</span></span>
<span data-ttu-id="8f54f-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f54f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f54f-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f54f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f54f-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f54f-147">INPUTS</span></span>

## <span data-ttu-id="8f54f-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f54f-148">OUTPUTS</span></span>

## <span data-ttu-id="8f54f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f54f-149">NOTES</span></span>

## <span data-ttu-id="8f54f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f54f-150">RELATED LINKS</span></span>

[<span data-ttu-id="8f54f-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8f54f-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="8f54f-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8f54f-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="8f54f-153">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8f54f-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="8f54f-154">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8f54f-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="8f54f-155">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8f54f-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


