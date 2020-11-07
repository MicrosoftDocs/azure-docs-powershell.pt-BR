---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947021"
---
# <span data-ttu-id="20b05-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="20b05-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="20b05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20b05-102">SYNOPSIS</span></span>


## <span data-ttu-id="20b05-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20b05-103">SYNTAX</span></span>

### <span data-ttu-id="20b05-104">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="20b05-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20b05-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20b05-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20b05-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20b05-106">DESCRIPTION</span></span>


## <span data-ttu-id="20b05-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20b05-107">EXAMPLES</span></span>

### <span data-ttu-id="20b05-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20b05-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="20b05-109">Exclua a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="20b05-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="20b05-110">OS</span><span class="sxs-lookup"><span data-stu-id="20b05-110">PARAMETERS</span></span>

### <span data-ttu-id="20b05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b05-111">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20b05-112">-Force</span><span class="sxs-lookup"><span data-stu-id="20b05-112">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20b05-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20b05-113">-InputObject</span></span>
<span data-ttu-id="20b05-114">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="20b05-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="20b05-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20b05-115">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20b05-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20b05-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20b05-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20b05-117">-Confirm</span></span>
<span data-ttu-id="20b05-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20b05-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20b05-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b05-119">-WhatIf</span></span>
<span data-ttu-id="20b05-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20b05-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b05-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20b05-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20b05-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b05-122">CommonParameters</span></span>
<span data-ttu-id="20b05-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b05-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b05-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20b05-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b05-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20b05-125">INPUTS</span></span>

### <span data-ttu-id="20b05-126">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="20b05-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="20b05-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20b05-127">OUTPUTS</span></span>

### <span data-ttu-id="20b05-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20b05-128">System.Boolean</span></span>



## <span data-ttu-id="20b05-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20b05-129">NOTES</span></span>

<span data-ttu-id="20b05-130">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="20b05-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20b05-131">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20b05-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="20b05-132">INPUTobject <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="20b05-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="20b05-133">`[DelegatedProviderId <String>]`: ID do provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="20b05-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="20b05-134">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="20b05-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20b05-135">`[OfferName <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="20b05-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="20b05-136">`[SubscriptionId <String>]`: ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="20b05-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="20b05-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20b05-137">RELATED LINKS</span></span>

