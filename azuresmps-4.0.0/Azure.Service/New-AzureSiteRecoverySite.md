---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945892"
---
# <span data-ttu-id="ff1b9-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="ff1b9-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="ff1b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1b9-103">Cria um site de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="ff1b9-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="ff1b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff1b9-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ff1b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff1b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ff1b9-106">O cmdlet **New-AzureSiteRecoverySite** cria um site de recuperação do site do Azure no cofre atual.</span><span class="sxs-lookup"><span data-stu-id="ff1b9-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="ff1b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff1b9-107">EXAMPLES</span></span>

### <span data-ttu-id="ff1b9-108">Exemplo 1: criar um site de recuperação do site</span><span class="sxs-lookup"><span data-stu-id="ff1b9-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="ff1b9-109">Esse comando cria um site de recuperação do site chamado RecoverySite07.</span><span class="sxs-lookup"><span data-stu-id="ff1b9-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="ff1b9-110">OS</span><span class="sxs-lookup"><span data-stu-id="ff1b9-110">PARAMETERS</span></span>

### <span data-ttu-id="ff1b9-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff1b9-111">-Name</span></span>
<span data-ttu-id="ff1b9-112">Especifica o nome do site.</span><span class="sxs-lookup"><span data-stu-id="ff1b9-112">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="ff1b9-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ff1b9-113">-Profile</span></span>
<span data-ttu-id="ff1b9-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ff1b9-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff1b9-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ff1b9-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff1b9-116">-Cofre</span><span class="sxs-lookup"><span data-stu-id="ff1b9-116">-Vault</span></span>
<span data-ttu-id="ff1b9-117">Especifica um cofre para o qual criar o site.</span><span class="sxs-lookup"><span data-stu-id="ff1b9-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="ff1b9-118">Para obter um objeto **ASRVault** , use o cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="ff1b9-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1b9-119">CommonParameters</span></span>
<span data-ttu-id="ff1b9-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff1b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1b9-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff1b9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1b9-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff1b9-122">INPUTS</span></span>

## <span data-ttu-id="ff1b9-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff1b9-123">OUTPUTS</span></span>

## <span data-ttu-id="ff1b9-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff1b9-124">NOTES</span></span>

## <span data-ttu-id="ff1b9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff1b9-125">RELATED LINKS</span></span>

[<span data-ttu-id="ff1b9-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="ff1b9-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="ff1b9-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="ff1b9-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


