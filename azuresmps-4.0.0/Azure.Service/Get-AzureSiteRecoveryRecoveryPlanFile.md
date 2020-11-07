---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945583"
---
# <span data-ttu-id="411c1-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="411c1-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="411c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="411c1-102">SYNOPSIS</span></span>
<span data-ttu-id="411c1-103">Baixa um plano do Azure site Recovery no formato XML.</span><span class="sxs-lookup"><span data-stu-id="411c1-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="411c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="411c1-104">SYNTAX</span></span>

### <span data-ttu-id="411c1-105">ByRPObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="411c1-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="411c1-106">ById</span><span class="sxs-lookup"><span data-stu-id="411c1-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="411c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="411c1-107">DESCRIPTION</span></span>
<span data-ttu-id="411c1-108">O cmdlet **Get-AzureSiteRecoveryRecoveryPlanFile** baixa um plano do Azure site Recovery no formato XML.</span><span class="sxs-lookup"><span data-stu-id="411c1-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="411c1-109">Você pode usar esse arquivo para atualizar o plano de recuperação e depois carregá-lo no servidor de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="411c1-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="411c1-110">Um plano de recuperação reúne máquinas virtuais em um grupo para fins de failover e recuperação.</span><span class="sxs-lookup"><span data-stu-id="411c1-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="411c1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="411c1-111">EXAMPLES</span></span>

### <span data-ttu-id="411c1-112">Exemplo 1: obter um arquivo de plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="411c1-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="411c1-113">Esse comando usa o cmdlet **Get-AzureSiteRecoveryRecoveryPlan** para obter o plano de recuperação e, em seguida, armazena-o na variável $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="411c1-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="411c1-114">O segundo comando usa o cmdlet **GetAzureSiteRecoveryRecoveryPlanFile** para obter o arquivo XML de plano de recuperação do site no $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="411c1-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="411c1-115">O comando armazena o arquivo XML no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="411c1-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="411c1-116">OS</span><span class="sxs-lookup"><span data-stu-id="411c1-116">PARAMETERS</span></span>

### <span data-ttu-id="411c1-117">-ID</span><span class="sxs-lookup"><span data-stu-id="411c1-117">-Id</span></span>
<span data-ttu-id="411c1-118">Especifica a ID do plano de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="411c1-118">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="411c1-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="411c1-119">-Path</span></span>
<span data-ttu-id="411c1-120">Especifica o caminho completo para armazenar o arquivo XML do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="411c1-120">Specifies the full path to store the recovery plan XML file.</span></span>

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

### <span data-ttu-id="411c1-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="411c1-121">-Profile</span></span>
<span data-ttu-id="411c1-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="411c1-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="411c1-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="411c1-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="411c1-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="411c1-124">-RecoveryPlan</span></span>
<span data-ttu-id="411c1-125">Especifica um objeto **ASRRecoveryPlan** do qual obter o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="411c1-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="411c1-126">Para obter um objeto **ASRRecoveryPlan** , use o cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="411c1-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="411c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="411c1-127">CommonParameters</span></span>
<span data-ttu-id="411c1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="411c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="411c1-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="411c1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="411c1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="411c1-130">INPUTS</span></span>

## <span data-ttu-id="411c1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="411c1-131">OUTPUTS</span></span>

## <span data-ttu-id="411c1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="411c1-132">NOTES</span></span>

## <span data-ttu-id="411c1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="411c1-133">RELATED LINKS</span></span>

[<span data-ttu-id="411c1-134">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="411c1-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)


