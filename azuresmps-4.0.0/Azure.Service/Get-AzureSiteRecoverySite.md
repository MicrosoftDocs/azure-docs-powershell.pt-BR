---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945577"
---
# <span data-ttu-id="9d959-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="9d959-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="9d959-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d959-102">SYNOPSIS</span></span>
<span data-ttu-id="9d959-103">Obtém os sites do Hyper-V de um cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="9d959-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="9d959-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d959-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d959-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d959-105">DESCRIPTION</span></span>
<span data-ttu-id="9d959-106">O cmdlet **Get-AzureSiteRecoverySite** Obtém os sites do Hyper-V em um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9d959-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9d959-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d959-107">EXAMPLES</span></span>

### <span data-ttu-id="9d959-108">Exemplo 1: obter sites de recuperação</span><span class="sxs-lookup"><span data-stu-id="9d959-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="9d959-109">Este comando obtém os sites de recuperação do cofre atual.</span><span class="sxs-lookup"><span data-stu-id="9d959-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="9d959-110">OS</span><span class="sxs-lookup"><span data-stu-id="9d959-110">PARAMETERS</span></span>

### <span data-ttu-id="9d959-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9d959-111">-Profile</span></span>
<span data-ttu-id="9d959-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9d959-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d959-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9d959-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d959-114">-Cofre</span><span class="sxs-lookup"><span data-stu-id="9d959-114">-Vault</span></span>
<span data-ttu-id="9d959-115">Especifica um cofre para obter sites.</span><span class="sxs-lookup"><span data-stu-id="9d959-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="9d959-116">Para obter um objeto **ASRVault** , use o cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="9d959-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="9d959-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d959-117">CommonParameters</span></span>
<span data-ttu-id="9d959-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d959-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d959-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d959-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d959-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d959-120">INPUTS</span></span>

## <span data-ttu-id="9d959-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d959-121">OUTPUTS</span></span>

## <span data-ttu-id="9d959-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d959-122">NOTES</span></span>

## <span data-ttu-id="9d959-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d959-123">RELATED LINKS</span></span>

[<span data-ttu-id="9d959-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="9d959-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="9d959-125">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="9d959-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


