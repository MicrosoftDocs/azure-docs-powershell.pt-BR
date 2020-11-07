---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945445"
---
# <span data-ttu-id="bde73-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="bde73-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="bde73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bde73-102">SYNOPSIS</span></span>
<span data-ttu-id="bde73-103">Altera as assinaturas atuais e padrão do Azure.</span><span class="sxs-lookup"><span data-stu-id="bde73-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="bde73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bde73-104">SYNTAX</span></span>

### <span data-ttu-id="bde73-105">SelectSubscriptionByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bde73-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bde73-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bde73-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bde73-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bde73-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bde73-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bde73-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bde73-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bde73-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="bde73-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bde73-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bde73-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bde73-111">DESCRIPTION</span></span>
<span data-ttu-id="bde73-112">O cmdlet **Select-AzureSubscription** define e limpa as assinaturas do Azure atuais e padrão.</span><span class="sxs-lookup"><span data-stu-id="bde73-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="bde73-113">A "assinatura atual" é a assinatura que é usada por padrão na sessão atual do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bde73-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="bde73-114">A "assinatura padrão" é usada por padrão em todas as sessões do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bde73-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="bde73-115">O rótulo "assinatura atual" permite que você especifique uma assinatura diferente para ser usada por padrão para a sessão atual sem alterar a "assinatura padrão" para todas as outras sessões.</span><span class="sxs-lookup"><span data-stu-id="bde73-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="bde73-116">A designação da assinatura "padrão" é salva no seu arquivo de dados de assinatura.</span><span class="sxs-lookup"><span data-stu-id="bde73-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="bde73-117">A designação "atual" específica da sessão não é salva.</span><span class="sxs-lookup"><span data-stu-id="bde73-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="bde73-118">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bde73-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bde73-119">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bde73-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="bde73-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bde73-120">EXAMPLES</span></span>

### <span data-ttu-id="bde73-121">Exemplo 1: definir a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="bde73-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="bde73-122">Esse comando torna "ContosoEngineering" a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="bde73-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="bde73-123">Exemplo 2: definir a assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="bde73-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="bde73-124">Esse comando altera a assinatura padrão para "ContosoFinance".</span><span class="sxs-lookup"><span data-stu-id="bde73-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="bde73-125">Ele salva a configuração no arquivo de dados de assinatura do Subscriptions.xml, em vez do arquivo de dados de assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="bde73-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="bde73-126">OS</span><span class="sxs-lookup"><span data-stu-id="bde73-126">PARAMETERS</span></span>

### <span data-ttu-id="bde73-127">-Conta</span><span class="sxs-lookup"><span data-stu-id="bde73-127">-Account</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde73-128">-Atual</span><span class="sxs-lookup"><span data-stu-id="bde73-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde73-129">-Padrão</span><span class="sxs-lookup"><span data-stu-id="bde73-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde73-130">-Noactual</span><span class="sxs-lookup"><span data-stu-id="bde73-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde73-131">-Não padrão</span><span class="sxs-lookup"><span data-stu-id="bde73-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde73-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bde73-132">-PassThru</span></span>
<span data-ttu-id="bde73-133">Retorna $True se o comando tiver êxito e $False se falhar.</span><span class="sxs-lookup"><span data-stu-id="bde73-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="bde73-134">Por padrão, esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="bde73-134">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="bde73-135">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bde73-135">-Profile</span></span>
<span data-ttu-id="bde73-136">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bde73-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bde73-137">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bde73-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bde73-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bde73-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde73-139">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="bde73-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde73-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde73-140">CommonParameters</span></span>
<span data-ttu-id="bde73-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bde73-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde73-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde73-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde73-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bde73-143">INPUTS</span></span>

### <span data-ttu-id="bde73-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bde73-144">None</span></span>
<span data-ttu-id="bde73-145">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="bde73-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="bde73-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bde73-146">OUTPUTS</span></span>

### <span data-ttu-id="bde73-147">None ou System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bde73-147">None or System.Boolean</span></span>
<span data-ttu-id="bde73-148">Se você usar o parâmetro *PassThru* , esse cmdlet retornará um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="bde73-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="bde73-149">Por padrão, ele não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="bde73-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="bde73-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bde73-150">NOTES</span></span>

## <span data-ttu-id="bde73-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bde73-151">RELATED LINKS</span></span>

[<span data-ttu-id="bde73-152">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="bde73-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="bde73-153">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="bde73-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="bde73-154">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="bde73-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


