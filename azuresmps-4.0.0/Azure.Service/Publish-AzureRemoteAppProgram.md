---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945884"
---
# <span data-ttu-id="245a7-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="245a7-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="245a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="245a7-102">SYNOPSIS</span></span>
<span data-ttu-id="245a7-103">Publica um programa do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="245a7-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="245a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="245a7-104">SYNTAX</span></span>

### <span data-ttu-id="245a7-105">ID do aplicativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="245a7-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="245a7-106">Caminho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="245a7-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="245a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="245a7-107">DESCRIPTION</span></span>
<span data-ttu-id="245a7-108">O cmdlet **Publish-AzureRemoteAppProgram** publica um programa Azure RemoteApp, que o torna disponível para os usuários da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="245a7-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="245a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="245a7-109">EXAMPLES</span></span>

### <span data-ttu-id="245a7-110">Exemplo 1: publicar um programa em uma coleção</span><span class="sxs-lookup"><span data-stu-id="245a7-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="245a7-111">Esse comando publica o programa na coleção ContosoApps com o *StartMenuAppId* especificado para adicionar o programa ao menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="245a7-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="245a7-112">O aplicativo publicado terá um nome para exibição de "aplicativo de Finanças".</span><span class="sxs-lookup"><span data-stu-id="245a7-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="245a7-113">OS</span><span class="sxs-lookup"><span data-stu-id="245a7-113">PARAMETERS</span></span>

### <span data-ttu-id="245a7-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="245a7-114">-CollectionName</span></span>
<span data-ttu-id="245a7-115">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="245a7-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="245a7-116">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="245a7-116">-CommandLine</span></span>
<span data-ttu-id="245a7-117">Especifica os argumentos de linha de comando para o programa que este cmdlet publica.</span><span class="sxs-lookup"><span data-stu-id="245a7-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="245a7-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="245a7-118">-DisplayName</span></span>
<span data-ttu-id="245a7-119">Especifica o nome de exibição amigável do programa Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="245a7-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="245a7-120">Os usuários veem isso como o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="245a7-120">Users see this as the name of the application.</span></span>

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

### <span data-ttu-id="245a7-121">-Filevirtualpath</span><span class="sxs-lookup"><span data-stu-id="245a7-121">-FileVirtualPath</span></span>
<span data-ttu-id="245a7-122">Especifica o caminho do programa dentro da imagem de modelo do programa.</span><span class="sxs-lookup"><span data-stu-id="245a7-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245a7-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="245a7-123">-Profile</span></span>
<span data-ttu-id="245a7-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="245a7-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="245a7-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="245a7-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="245a7-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="245a7-126">-StartMenuAppId</span></span>
<span data-ttu-id="245a7-127">Especifica um GUID que esse cmdlet usa para adicionar o programa ao menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="245a7-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245a7-128">CommonParameters</span></span>
<span data-ttu-id="245a7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="245a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245a7-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="245a7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245a7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="245a7-131">INPUTS</span></span>

## <span data-ttu-id="245a7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="245a7-132">OUTPUTS</span></span>

## <span data-ttu-id="245a7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="245a7-133">NOTES</span></span>

## <span data-ttu-id="245a7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="245a7-134">RELATED LINKS</span></span>

[<span data-ttu-id="245a7-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="245a7-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="245a7-136">Cancelar publicação-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="245a7-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


