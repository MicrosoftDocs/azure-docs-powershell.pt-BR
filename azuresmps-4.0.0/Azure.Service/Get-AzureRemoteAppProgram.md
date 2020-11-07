---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946319"
---
# <span data-ttu-id="04329-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="04329-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="04329-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04329-102">SYNOPSIS</span></span>
<span data-ttu-id="04329-103">Recupera as propriedades de um ou mais programas RemoteApp do Azure publicados para uma coleção.</span><span class="sxs-lookup"><span data-stu-id="04329-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="04329-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04329-104">SYNTAX</span></span>

### <span data-ttu-id="04329-105">FilterByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="04329-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="04329-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="04329-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="04329-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04329-107">DESCRIPTION</span></span>
<span data-ttu-id="04329-108">O cmdlet **Get-AzureRemoteAppProgram** recupera as propriedades de um ou mais programas RemoteApp do Azure publicados para uma coleção.</span><span class="sxs-lookup"><span data-stu-id="04329-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="04329-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04329-109">EXAMPLES</span></span>

### <span data-ttu-id="04329-110">Exemplo 1: recuperar as propriedades de um programa</span><span class="sxs-lookup"><span data-stu-id="04329-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="04329-111">Esse comando exibe as propriedades de um programa RemoteApp do Azure.</span><span class="sxs-lookup"><span data-stu-id="04329-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="04329-112">O programa, chamado de aplicativo finanças, está na coleção do Azure RemoteApp chamada ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="04329-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="04329-113">OS</span><span class="sxs-lookup"><span data-stu-id="04329-113">PARAMETERS</span></span>

### <span data-ttu-id="04329-114">-Alias</span><span class="sxs-lookup"><span data-stu-id="04329-114">-Alias</span></span>
<span data-ttu-id="04329-115">Especifica o alias do programa para o qual recuperar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="04329-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04329-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="04329-116">-CollectionName</span></span>
<span data-ttu-id="04329-117">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="04329-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04329-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="04329-118">-Profile</span></span>
<span data-ttu-id="04329-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="04329-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04329-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="04329-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04329-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="04329-121">-RemoteAppProgram</span></span>
<span data-ttu-id="04329-122">Especifica o nome do programa para o qual recuperar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="04329-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="04329-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04329-123">CommonParameters</span></span>
<span data-ttu-id="04329-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04329-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04329-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04329-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04329-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04329-126">INPUTS</span></span>

## <span data-ttu-id="04329-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04329-127">OUTPUTS</span></span>

## <span data-ttu-id="04329-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04329-128">NOTES</span></span>

## <span data-ttu-id="04329-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04329-129">RELATED LINKS</span></span>

[<span data-ttu-id="04329-130">Publicar-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="04329-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="04329-131">Cancelar publicação-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="04329-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


