---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946111"
---
# <span data-ttu-id="15f2f-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15f2f-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="15f2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="15f2f-103">Remove um plano de recuperação de site da recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="15f2f-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="15f2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15f2f-104">SYNTAX</span></span>

### <span data-ttu-id="15f2f-105">ByRPObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="15f2f-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15f2f-106">ById</span><span class="sxs-lookup"><span data-stu-id="15f2f-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15f2f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="15f2f-108">O cmdlet **Remove-AzureSiteRecoveryRecoveryPlan** remove um plano de recuperação de site do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="15f2f-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="15f2f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15f2f-109">EXAMPLES</span></span>

### <span data-ttu-id="15f2f-110">Exemplo 1: remover um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="15f2f-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="15f2f-111">O primeiro comando usa o cmdlet **Get-AzureSiteRecoveryRecoveryPlan** para obter o plano de recuperação do site e, em seguida, armazena-o na variável $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="15f2f-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="15f2f-112">O segundo comando Remove o plano de recuperação em $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="15f2f-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="15f2f-113">OS</span><span class="sxs-lookup"><span data-stu-id="15f2f-113">PARAMETERS</span></span>

### <span data-ttu-id="15f2f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="15f2f-114">-Force</span></span>
<span data-ttu-id="15f2f-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="15f2f-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f2f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="15f2f-116">-Id</span></span>
<span data-ttu-id="15f2f-117">Especifica a ID do plano de recuperação a ser removida.</span><span class="sxs-lookup"><span data-stu-id="15f2f-117">Specifies the ID of the recovery plan to remove.</span></span>

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

### <span data-ttu-id="15f2f-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="15f2f-118">-Profile</span></span>
<span data-ttu-id="15f2f-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="15f2f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15f2f-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="15f2f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="15f2f-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15f2f-121">-RecoveryPlan</span></span>
<span data-ttu-id="15f2f-122">Especifica o plano de recuperação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="15f2f-122">Specifies the recovery plan to remove.</span></span>

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

### <span data-ttu-id="15f2f-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="15f2f-123">-WaitForCompletion</span></span>
<span data-ttu-id="15f2f-124">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15f2f-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f2f-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15f2f-125">-Confirm</span></span>
<span data-ttu-id="15f2f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15f2f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f2f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15f2f-127">-WhatIf</span></span>
<span data-ttu-id="15f2f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15f2f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15f2f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15f2f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f2f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f2f-130">CommonParameters</span></span>
<span data-ttu-id="15f2f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15f2f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f2f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15f2f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f2f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15f2f-133">INPUTS</span></span>

## <span data-ttu-id="15f2f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15f2f-134">OUTPUTS</span></span>

## <span data-ttu-id="15f2f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15f2f-135">NOTES</span></span>

## <span data-ttu-id="15f2f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15f2f-136">RELATED LINKS</span></span>

[<span data-ttu-id="15f2f-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15f2f-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="15f2f-138">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15f2f-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="15f2f-139">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="15f2f-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


