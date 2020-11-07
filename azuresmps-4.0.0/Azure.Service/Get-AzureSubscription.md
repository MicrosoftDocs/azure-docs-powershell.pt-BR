---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945537"
---
# <span data-ttu-id="8c668-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8c668-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="8c668-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c668-102">SYNOPSIS</span></span>
<span data-ttu-id="8c668-103">Obtém assinaturas do Azure na conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c668-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="8c668-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c668-104">SYNTAX</span></span>

### <span data-ttu-id="8c668-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c668-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c668-106">ById</span><span class="sxs-lookup"><span data-stu-id="8c668-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c668-107">Assume</span><span class="sxs-lookup"><span data-stu-id="8c668-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8c668-108">Atualizados</span><span class="sxs-lookup"><span data-stu-id="8c668-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c668-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c668-109">DESCRIPTION</span></span>
<span data-ttu-id="8c668-110">O cmdlet **Get-AzureSubscription** Obtém as assinaturas na sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c668-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="8c668-111">Você pode usar esse cmdlet para obter informações sobre a assinatura e para canalizar a assinatura para outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="8c668-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="8c668-112">**Get-AzureSubscription** requer acesso às suas contas do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c668-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="8c668-113">Antes de executar **Get-AzureSubscription** , você deve executar o cmdlet **Add-AzureAccount** ou os cmdlets que baixam e instalam um arquivo de configurações de publicação ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span><span class="sxs-lookup"><span data-stu-id="8c668-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="8c668-114">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c668-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8c668-115">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8c668-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="8c668-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c668-116">EXAMPLES</span></span>

### <span data-ttu-id="8c668-117">Exemplo 1: obter todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="8c668-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="8c668-118">Esse comando obtém todas as assinaturas na conta.</span><span class="sxs-lookup"><span data-stu-id="8c668-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="8c668-119">Exemplo 2: obter uma assinatura por nome</span><span class="sxs-lookup"><span data-stu-id="8c668-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="8c668-120">Esse comando obtém apenas a assinatura "MyProdSubsciption".</span><span class="sxs-lookup"><span data-stu-id="8c668-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="8c668-121">Exemplo 3: obter a assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="8c668-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="8c668-122">Esse comando obtém apenas o nome da assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="8c668-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="8c668-123">O comando recebe primeiro a assinatura e, em seguida, usa o método dot para obter a propriedade **subscriptionname** da assinatura.</span><span class="sxs-lookup"><span data-stu-id="8c668-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="8c668-124">Exemplo 4: obter as propriedades da assinatura selecionada</span><span class="sxs-lookup"><span data-stu-id="8c668-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="8c668-125">Esse comando retorna uma lista com o nome e o certificado da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8c668-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="8c668-126">Ele usa um comando **Get-AzureSubscription** para obter a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8c668-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="8c668-127">Em seguida, ele canaliza a assinatura para um comando de **lista de formatação** que exibe as propriedades selecionadas em uma lista.</span><span class="sxs-lookup"><span data-stu-id="8c668-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="8c668-128">Exemplo 5: usar um arquivo de dados de assinatura alternativo</span><span class="sxs-lookup"><span data-stu-id="8c668-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="8c668-129">Este comando obtém assinaturas do arquivo de dados de assinatura do C:\Temp\MySubscriptions.xml.</span><span class="sxs-lookup"><span data-stu-id="8c668-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="8c668-130">Use o parâmetro **SubscriptionDataFile** se você tiver especificado um arquivo de dados de assinatura alternativo ao executar os cmdlets **Add-AzureAccount** ou **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="8c668-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="8c668-131">OS</span><span class="sxs-lookup"><span data-stu-id="8c668-131">PARAMETERS</span></span>

### <span data-ttu-id="8c668-132">-Atual</span><span class="sxs-lookup"><span data-stu-id="8c668-132">-Current</span></span>
<span data-ttu-id="8c668-133">Obtém apenas a assinatura atual, ou seja, a assinatura designada como "atual".</span><span class="sxs-lookup"><span data-stu-id="8c668-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="8c668-134">Por padrão, **Get-AzureSubscription** obtém todas as assinaturas em suas contas do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c668-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="8c668-135">Para designar uma assinatura como "atual", use o parâmetro **atual** do cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="8c668-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c668-136">-Padrão</span><span class="sxs-lookup"><span data-stu-id="8c668-136">-Default</span></span>
<span data-ttu-id="8c668-137">Obtém apenas a assinatura padrão, ou seja, a assinatura designada como "padrão".</span><span class="sxs-lookup"><span data-stu-id="8c668-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="8c668-138">Por padrão, **Get-AzureSubscription** obtém todas as assinaturas em suas contas do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c668-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="8c668-139">Para designar uma assinatura como "padrão", use o parâmetro **padrão** do cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="8c668-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c668-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="8c668-140">-ExtendedDetails</span></span>
<span data-ttu-id="8c668-141">Retorna as informações de cota da assinatura, além das configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="8c668-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="8c668-142">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8c668-142">-Profile</span></span>
<span data-ttu-id="8c668-143">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8c668-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8c668-144">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8c668-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c668-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c668-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c668-146">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="8c668-146">-SubscriptionName</span></span>
<span data-ttu-id="8c668-147">Obtém apenas a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="8c668-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="8c668-148">Digite o nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="8c668-148">Enter the subscription name.</span></span>
<span data-ttu-id="8c668-149">O valor diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8c668-149">The value is case-sensitive.</span></span>
<span data-ttu-id="8c668-150">Não há suporte para caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="8c668-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="8c668-151">Por padrão, **Get-AzureSubscription** obtém todas as assinaturas em suas contas do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c668-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c668-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c668-152">CommonParameters</span></span>
<span data-ttu-id="8c668-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c668-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c668-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c668-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c668-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c668-155">INPUTS</span></span>

### <span data-ttu-id="8c668-156">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8c668-156">None</span></span>
<span data-ttu-id="8c668-157">Você pode canalizar a entrada para a propriedade **subscriptionname** por nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="8c668-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="8c668-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c668-158">OUTPUTS</span></span>

### <span data-ttu-id="8c668-159">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8c668-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="8c668-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c668-160">NOTES</span></span>
* <span data-ttu-id="8c668-161">Get-AzureSubscription obtém dados do arquivo de dados de assinatura que os cmdlets **Add-AzureAccount** e **Import-PublishSettingsFile** criam.</span><span class="sxs-lookup"><span data-stu-id="8c668-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="8c668-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c668-162">RELATED LINKS</span></span>

[<span data-ttu-id="8c668-163">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="8c668-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="8c668-164">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8c668-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="8c668-165">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8c668-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="8c668-166">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8c668-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="8c668-167">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8c668-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


