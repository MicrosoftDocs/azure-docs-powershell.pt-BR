---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946329"
---
# <span data-ttu-id="3fc9e-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3fc9e-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="3fc9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc9e-103">Recupera informações sobre uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3fc9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fc9e-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3fc9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fc9e-105">DESCRIPTION</span></span>
<span data-ttu-id="3fc9e-106">O cmdlet **Get-AzureRemoteAppCollection** recupera informações sobre coleções do Azure RemoteApp no Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="3fc9e-107">Ele retorna um objeto com informações em uma coleção específica, ou se nenhuma coleção for especificada, para todas as coleções na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="3fc9e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fc9e-108">EXAMPLES</span></span>

### <span data-ttu-id="3fc9e-109">Exemplo 1: obter uma lista de todas as coleções</span><span class="sxs-lookup"><span data-stu-id="3fc9e-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="3fc9e-110">Esse comando retorna uma lista de todas as coleções do RemoteApp do Azure na assinatura.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="3fc9e-111">Exemplo 2: obter informações sobre uma coleção especificada</span><span class="sxs-lookup"><span data-stu-id="3fc9e-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="3fc9e-112">Esse comando retorna informações sobre a coleção do Azure RemoteApp chamada ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="3fc9e-113">Exemplo 3: obter uma lista de coleções usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="3fc9e-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="3fc9e-114">Esse comando retorna uma lista de todas as coleções do RemoteApp do Azure correspondentes às finanças \*.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="3fc9e-115">OS</span><span class="sxs-lookup"><span data-stu-id="3fc9e-115">PARAMETERS</span></span>

### <span data-ttu-id="3fc9e-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3fc9e-116">-CollectionName</span></span>
<span data-ttu-id="3fc9e-117">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3fc9e-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3fc9e-118">-Profile</span></span>
<span data-ttu-id="3fc9e-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3fc9e-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3fc9e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc9e-121">CommonParameters</span></span>
<span data-ttu-id="3fc9e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc9e-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc9e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc9e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fc9e-124">INPUTS</span></span>

## <span data-ttu-id="3fc9e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fc9e-125">OUTPUTS</span></span>

## <span data-ttu-id="3fc9e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fc9e-126">NOTES</span></span>

## <span data-ttu-id="3fc9e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fc9e-127">RELATED LINKS</span></span>

[<span data-ttu-id="3fc9e-128">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3fc9e-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="3fc9e-129">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3fc9e-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="3fc9e-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3fc9e-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="3fc9e-131">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3fc9e-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


