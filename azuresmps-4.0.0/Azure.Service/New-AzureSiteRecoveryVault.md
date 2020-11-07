---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945974"
---
# <span data-ttu-id="6c233-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6c233-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="6c233-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c233-102">SYNOPSIS</span></span>
<span data-ttu-id="6c233-103">Cria um cofre de serviços de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="6c233-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="6c233-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c233-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6c233-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c233-105">DESCRIPTION</span></span>
<span data-ttu-id="6c233-106">O cmdlet **New-AzureSiteRecoveryVault** cria um cofre de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="6c233-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="6c233-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c233-107">EXAMPLES</span></span>

### <span data-ttu-id="6c233-108">Exemplo 1: criar um cofre</span><span class="sxs-lookup"><span data-stu-id="6c233-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="6c233-109">Esse comando cria um cofre chamado ContosoVault no local do oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="6c233-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="6c233-110">OS</span><span class="sxs-lookup"><span data-stu-id="6c233-110">PARAMETERS</span></span>

### <span data-ttu-id="6c233-111">-Local</span><span class="sxs-lookup"><span data-stu-id="6c233-111">-Location</span></span>
<span data-ttu-id="6c233-112">Especifica a localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="6c233-112">Specifies the geographical location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c233-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c233-113">-Name</span></span>
<span data-ttu-id="6c233-114">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="6c233-114">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c233-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6c233-115">-Profile</span></span>
<span data-ttu-id="6c233-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6c233-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c233-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6c233-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c233-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c233-118">CommonParameters</span></span>
<span data-ttu-id="6c233-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c233-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c233-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c233-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c233-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c233-121">INPUTS</span></span>

## <span data-ttu-id="6c233-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c233-122">OUTPUTS</span></span>

## <span data-ttu-id="6c233-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c233-123">NOTES</span></span>

## <span data-ttu-id="6c233-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c233-124">RELATED LINKS</span></span>

[<span data-ttu-id="6c233-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6c233-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


