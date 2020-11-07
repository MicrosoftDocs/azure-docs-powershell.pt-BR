---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946014"
---
# <span data-ttu-id="7435a-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7435a-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="7435a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7435a-102">SYNOPSIS</span></span>
<span data-ttu-id="7435a-103">Atualiza um plano de recuperação na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="7435a-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="7435a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7435a-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7435a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7435a-105">DESCRIPTION</span></span>
<span data-ttu-id="7435a-106">O cmdlet **Update-AzureSiteRecoveryRecoveryPlan** atualiza um plano de recuperação no Azure site Recovery e, em seguida, o publica.</span><span class="sxs-lookup"><span data-stu-id="7435a-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="7435a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7435a-107">EXAMPLES</span></span>

### <span data-ttu-id="7435a-108">Exemplo 1: atualizar um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="7435a-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="7435a-109">Esse comando atualiza o plano de recuperação especificado e o publica.</span><span class="sxs-lookup"><span data-stu-id="7435a-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="7435a-110">OS</span><span class="sxs-lookup"><span data-stu-id="7435a-110">PARAMETERS</span></span>

### <span data-ttu-id="7435a-111">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="7435a-111">-File</span></span>
<span data-ttu-id="7435a-112">Especifica o arquivo de plano de recuperação do plano de recuperação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="7435a-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7435a-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7435a-113">-Profile</span></span>
<span data-ttu-id="7435a-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7435a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7435a-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7435a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7435a-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7435a-116">-WaitForCompletion</span></span>
<span data-ttu-id="7435a-117">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7435a-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7435a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7435a-118">CommonParameters</span></span>
<span data-ttu-id="7435a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7435a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7435a-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7435a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7435a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7435a-121">INPUTS</span></span>

## <span data-ttu-id="7435a-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7435a-122">OUTPUTS</span></span>

## <span data-ttu-id="7435a-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7435a-123">NOTES</span></span>

## <span data-ttu-id="7435a-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7435a-124">RELATED LINKS</span></span>

[<span data-ttu-id="7435a-125">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7435a-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7435a-126">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7435a-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7435a-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7435a-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


