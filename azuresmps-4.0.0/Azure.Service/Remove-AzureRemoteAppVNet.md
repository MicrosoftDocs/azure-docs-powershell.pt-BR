---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946146"
---
# <span data-ttu-id="ba387-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ba387-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="ba387-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba387-102">SYNOPSIS</span></span>
<span data-ttu-id="ba387-103">Exclui uma rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ba387-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="ba387-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba387-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ba387-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba387-105">DESCRIPTION</span></span>
<span data-ttu-id="ba387-106">O cmdlet **Remove-AzureRemoteAppVNet** exclui uma rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ba387-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="ba387-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba387-107">EXAMPLES</span></span>

### <span data-ttu-id="ba387-108">Exemplo 1: excluir uma rede virtual especificada</span><span class="sxs-lookup"><span data-stu-id="ba387-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="ba387-109">Esse comando exclui a rede virtual chamada ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="ba387-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="ba387-110">OS</span><span class="sxs-lookup"><span data-stu-id="ba387-110">PARAMETERS</span></span>

### <span data-ttu-id="ba387-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ba387-111">-Profile</span></span>
<span data-ttu-id="ba387-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ba387-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba387-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ba387-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba387-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ba387-114">-VNetName</span></span>
<span data-ttu-id="ba387-115">Especifica o nome da rede virtual do Azure RemoteApp a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="ba387-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba387-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba387-116">CommonParameters</span></span>
<span data-ttu-id="ba387-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba387-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba387-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba387-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba387-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba387-119">INPUTS</span></span>

## <span data-ttu-id="ba387-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba387-120">OUTPUTS</span></span>

## <span data-ttu-id="ba387-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba387-121">NOTES</span></span>

## <span data-ttu-id="ba387-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba387-122">RELATED LINKS</span></span>

[<span data-ttu-id="ba387-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ba387-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="ba387-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ba387-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


