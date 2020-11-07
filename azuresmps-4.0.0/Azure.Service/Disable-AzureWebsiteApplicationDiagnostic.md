---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945690"
---
# <span data-ttu-id="7b4e9-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b4e9-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="7b4e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4e9-103">Desabilita o diagnóstico de aplicativos para um site do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="7b4e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b4e9-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7b4e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b4e9-105">DESCRIPTION</span></span>
<span data-ttu-id="7b4e9-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7b4e9-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7b4e9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7b4e9-108">Desabilita o diagnóstico de aplicativos para um site do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="7b4e9-109">Desabilita o log configurado para ser armazenado em um sistema de arquivos ou no Azure.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="7b4e9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b4e9-110">EXAMPLES</span></span>

### <span data-ttu-id="7b4e9-111">Exemplo 1: desabilitar o arquivo de log do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7b4e9-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="7b4e9-112">O exemplo a seguir desabilita o log do aplicativo no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="7b4e9-113">Exemplo 2: desabilitar o registro em log usando o Azure Storage</span><span class="sxs-lookup"><span data-stu-id="7b4e9-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="7b4e9-114">O exemplo a seguir desabilita o log do aplicativo usando armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="7b4e9-115">OS</span><span class="sxs-lookup"><span data-stu-id="7b4e9-115">PARAMETERS</span></span>

### <span data-ttu-id="7b4e9-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="7b4e9-116">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b4e9-117">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="7b4e9-117">-File</span></span>
<span data-ttu-id="7b4e9-118">Especifica que você deseja usar o sistema de arquivos para armazenar os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-118">Specifies that you want to use the file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b4e9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b4e9-119">-Name</span></span>
<span data-ttu-id="7b4e9-120">Especifica o nome do site.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-120">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="7b4e9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b4e9-121">-PassThru</span></span>
<span data-ttu-id="7b4e9-122">Sinalizador para retornar true se bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-122">Flag to return true if succeeded.</span></span>

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

### <span data-ttu-id="7b4e9-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7b4e9-123">-Profile</span></span>
<span data-ttu-id="7b4e9-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7b4e9-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7b4e9-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="7b4e9-126">-Slot</span></span>
<span data-ttu-id="7b4e9-127">Especifica o nome do slot.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-127">Specifies the name of slot.</span></span>

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

### <span data-ttu-id="7b4e9-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="7b4e9-128">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b4e9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4e9-129">CommonParameters</span></span>
<span data-ttu-id="7b4e9-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4e9-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b4e9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4e9-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b4e9-132">INPUTS</span></span>

## <span data-ttu-id="7b4e9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b4e9-133">OUTPUTS</span></span>

## <span data-ttu-id="7b4e9-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b4e9-134">NOTES</span></span>

## <span data-ttu-id="7b4e9-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b4e9-135">RELATED LINKS</span></span>

[<span data-ttu-id="7b4e9-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b4e9-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="7b4e9-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7b4e9-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="7b4e9-138">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7b4e9-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="7b4e9-139">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7b4e9-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="7b4e9-140">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7b4e9-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


