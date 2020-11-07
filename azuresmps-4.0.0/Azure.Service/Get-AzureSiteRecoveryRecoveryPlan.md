---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945585"
---
# <span data-ttu-id="eeb0d-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eeb0d-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="eeb0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eeb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb0d-103">Obtém um plano de recuperação na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="eeb0d-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="eeb0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eeb0d-104">SYNTAX</span></span>

### <span data-ttu-id="eeb0d-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="eeb0d-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="eeb0d-106">ById</span><span class="sxs-lookup"><span data-stu-id="eeb0d-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="eeb0d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="eeb0d-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eeb0d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eeb0d-108">DESCRIPTION</span></span>
<span data-ttu-id="eeb0d-109">O cmdlet **Get-AzureSiteRecoveryRecoveryPlan** Obtém um plano de recuperação no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="eeb0d-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="eeb0d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eeb0d-110">EXAMPLES</span></span>

### <span data-ttu-id="eeb0d-111">Exemplo 1: obter um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="eeb0d-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="eeb0d-112">Esse comando obtém informações sobre o plano de recuperação do cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="eeb0d-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="eeb0d-113">OS</span><span class="sxs-lookup"><span data-stu-id="eeb0d-113">PARAMETERS</span></span>

### <span data-ttu-id="eeb0d-114">-ID</span><span class="sxs-lookup"><span data-stu-id="eeb0d-114">-Id</span></span>
<span data-ttu-id="eeb0d-115">Especifica a ID do plano de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="eeb0d-115">Specifies the ID of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb0d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="eeb0d-116">-Name</span></span>
<span data-ttu-id="eeb0d-117">Especifica o nome do plano de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="eeb0d-117">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="eeb0d-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="eeb0d-118">-Profile</span></span>
<span data-ttu-id="eeb0d-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="eeb0d-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eeb0d-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="eeb0d-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eeb0d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb0d-121">CommonParameters</span></span>
<span data-ttu-id="eeb0d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb0d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb0d-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb0d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb0d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eeb0d-124">INPUTS</span></span>

## <span data-ttu-id="eeb0d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eeb0d-125">OUTPUTS</span></span>

## <span data-ttu-id="eeb0d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eeb0d-126">NOTES</span></span>

## <span data-ttu-id="eeb0d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eeb0d-127">RELATED LINKS</span></span>

[<span data-ttu-id="eeb0d-128">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eeb0d-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="eeb0d-129">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eeb0d-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="eeb0d-130">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eeb0d-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


