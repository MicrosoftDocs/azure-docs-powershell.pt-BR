---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946565"
---
# <span data-ttu-id="1fe53-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="1fe53-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="1fe53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fe53-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe53-103">Obtém cofres de recuperação de site da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1fe53-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="1fe53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fe53-104">SYNTAX</span></span>

### <span data-ttu-id="1fe53-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="1fe53-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1fe53-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1fe53-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1fe53-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fe53-107">DESCRIPTION</span></span>
<span data-ttu-id="1fe53-108">O cmdlet **Get-AzureSiteRecoveryVault** Obtém uma lista de cofres do Azure site Recovery ou um cofre de recuperação de site específico da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1fe53-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="1fe53-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fe53-109">EXAMPLES</span></span>

### <span data-ttu-id="1fe53-110">Exemplo 1: obter o cofre ativo</span><span class="sxs-lookup"><span data-stu-id="1fe53-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="1fe53-111">Esse comando obtém o cofre ativo do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1fe53-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="1fe53-112">OS</span><span class="sxs-lookup"><span data-stu-id="1fe53-112">PARAMETERS</span></span>

### <span data-ttu-id="1fe53-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fe53-113">-Name</span></span>
<span data-ttu-id="1fe53-114">Especifica o nome do cofre a obter.</span><span class="sxs-lookup"><span data-stu-id="1fe53-114">Specifies the name of the vault to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe53-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1fe53-115">-Profile</span></span>
<span data-ttu-id="1fe53-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1fe53-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1fe53-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1fe53-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1fe53-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe53-118">CommonParameters</span></span>
<span data-ttu-id="1fe53-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe53-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe53-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe53-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe53-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fe53-121">INPUTS</span></span>

## <span data-ttu-id="1fe53-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fe53-122">OUTPUTS</span></span>

## <span data-ttu-id="1fe53-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fe53-123">NOTES</span></span>

## <span data-ttu-id="1fe53-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fe53-124">RELATED LINKS</span></span>

[<span data-ttu-id="1fe53-125">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="1fe53-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


