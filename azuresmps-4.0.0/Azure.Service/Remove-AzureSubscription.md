---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946095"
---
# <span data-ttu-id="45aba-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="45aba-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="45aba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45aba-102">SYNOPSIS</span></span>
<span data-ttu-id="45aba-103">Exclui uma assinatura do Azure do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45aba-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="45aba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45aba-104">SYNTAX</span></span>

### <span data-ttu-id="45aba-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="45aba-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45aba-106">%</span><span class="sxs-lookup"><span data-stu-id="45aba-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45aba-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45aba-107">DESCRIPTION</span></span>
<span data-ttu-id="45aba-108">O cmdlet **Remove-AzureSubscription** exclui uma assinatura do Azure do seu arquivo de dados de assinatura, portanto, o Windows PowerShell não consegue encontrá-la.</span><span class="sxs-lookup"><span data-stu-id="45aba-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="45aba-109">Esse cmdlet não exclui a assinatura do Microsoft Azure, nem altera a assinatura real de maneira alguma.</span><span class="sxs-lookup"><span data-stu-id="45aba-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="45aba-110">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45aba-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="45aba-111">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="45aba-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="45aba-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45aba-112">EXAMPLES</span></span>

### <span data-ttu-id="45aba-113">Exemplo 1: excluir uma assinatura</span><span class="sxs-lookup"><span data-stu-id="45aba-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="45aba-114">Esse comando exclui a assinatura "Test" do arquivo de dados de assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="45aba-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="45aba-115">Exemplo 2: excluir de um arquivo de dados de assinatura alternativo</span><span class="sxs-lookup"><span data-stu-id="45aba-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="45aba-116">Esse comando exclui a assinatura de teste do arquivo de dados de assinatura do MySubscriptions.xml.</span><span class="sxs-lookup"><span data-stu-id="45aba-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="45aba-117">O comando usa o parâmetro *Force* para suprimir o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="45aba-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="45aba-118">Exemplo 3: excluir uma assinatura em um script</span><span class="sxs-lookup"><span data-stu-id="45aba-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="45aba-119">Esse comando usa o comando **Remove-AzureSubscription** em uma instrução **se** .</span><span class="sxs-lookup"><span data-stu-id="45aba-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="45aba-120">Ele usa o parâmetro *PassThru* , que retorna um valor booliano, para determinar se o bloco de script na instrução **se** é executado.</span><span class="sxs-lookup"><span data-stu-id="45aba-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="45aba-121">OS</span><span class="sxs-lookup"><span data-stu-id="45aba-121">PARAMETERS</span></span>

### <span data-ttu-id="45aba-122">-Force</span><span class="sxs-lookup"><span data-stu-id="45aba-122">-Force</span></span>
<span data-ttu-id="45aba-123">Suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="45aba-123">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="45aba-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45aba-124">-PassThru</span></span>
<span data-ttu-id="45aba-125">Retorna $True se o comando tiver êxito e $False se falhar.</span><span class="sxs-lookup"><span data-stu-id="45aba-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="45aba-126">Por padrão, esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="45aba-126">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="45aba-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="45aba-127">-Profile</span></span>
<span data-ttu-id="45aba-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="45aba-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="45aba-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="45aba-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45aba-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45aba-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45aba-131">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="45aba-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45aba-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45aba-132">-Confirm</span></span>
<span data-ttu-id="45aba-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45aba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45aba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45aba-134">-WhatIf</span></span>
<span data-ttu-id="45aba-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45aba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45aba-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45aba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45aba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45aba-137">CommonParameters</span></span>
<span data-ttu-id="45aba-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45aba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45aba-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45aba-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45aba-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45aba-140">INPUTS</span></span>

### <span data-ttu-id="45aba-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="45aba-141">None</span></span>
<span data-ttu-id="45aba-142">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="45aba-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="45aba-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45aba-143">OUTPUTS</span></span>

### <span data-ttu-id="45aba-144">None ou System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45aba-144">None or System.Boolean</span></span>
<span data-ttu-id="45aba-145">Se você usar o parâmetro *PassThru* , esse cmdlet retornará um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="45aba-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="45aba-146">Caso contrário, ele não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="45aba-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="45aba-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45aba-147">NOTES</span></span>

## <span data-ttu-id="45aba-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45aba-148">RELATED LINKS</span></span>

[<span data-ttu-id="45aba-149">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="45aba-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="45aba-150">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="45aba-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="45aba-151">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="45aba-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


