---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945950"
---
# <span data-ttu-id="02d64-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="02d64-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="02d64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02d64-102">SYNOPSIS</span></span>
<span data-ttu-id="02d64-103">Altera uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="02d64-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="02d64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02d64-104">SYNTAX</span></span>

### <span data-ttu-id="02d64-105">UpdateSubscriptionByIdParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="02d64-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="02d64-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="02d64-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="02d64-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="02d64-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="02d64-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02d64-108">DESCRIPTION</span></span>
<span data-ttu-id="02d64-109">O cmdlet **set-AzureSubscription** estabelece e altera as propriedades de um objeto de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="02d64-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="02d64-110">Você pode usar esse cmdlet para trabalhar em uma assinatura do Azure que não seja a sua assinatura padrão ou alterar sua conta de armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="02d64-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="02d64-111">Para obter informações sobre as assinaturas atual e padrão, consulte o cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="02d64-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="02d64-112">Esse cmdlet opera em um objeto de assinatura do Azure, não na sua assinatura real do Azure.</span><span class="sxs-lookup"><span data-stu-id="02d64-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="02d64-113">Para criar e provisionar uma assinatura do Azure, acesse o [portal do Azure](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="02d64-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="02d64-114">Esse cmdlet altera os dados no arquivo de dados de assinatura que você cria quando usa o cmdlet **Add-AzureAccount** ou **Import-AzurePublishSettingsFile** para adicionar uma conta do Azure ao Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02d64-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="02d64-115">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02d64-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="02d64-116">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="02d64-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="02d64-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02d64-117">EXAMPLES</span></span>

### <span data-ttu-id="02d64-118">Exemplo 1: alterar um subscription1 existente</span><span class="sxs-lookup"><span data-stu-id="02d64-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="02d64-119">Este exemplo altera o certificado para a assinatura chamada ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="02d64-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="02d64-120">Exemplo 2: alterar o ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="02d64-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="02d64-121">Esse comando adiciona ou altera um ponto de extremidade de serviço personalizado para a assinatura do ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="02d64-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="02d64-122">Exemplo 3: limpar valores de propriedade</span><span class="sxs-lookup"><span data-stu-id="02d64-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="02d64-123">Esse comando define os valores das propriedades Certificate e ResourceManagerEndpoint como NULL ($Null).</span><span class="sxs-lookup"><span data-stu-id="02d64-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="02d64-124">Isso limpa os valores dessas propriedades sem alterar outras configurações.</span><span class="sxs-lookup"><span data-stu-id="02d64-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="02d64-125">Exemplo 4: usar um arquivo de dados de assinatura alternativo</span><span class="sxs-lookup"><span data-stu-id="02d64-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="02d64-126">Esse comando altera a conta de armazenamento atual da assinatura do ContosoFinance para o ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="02d64-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="02d64-127">O comando usa o parâmetro **SubscriptionDataFile** para alterar os dados no arquivo de dados de assinatura do C:\Azure\SubscriptionData.xml.</span><span class="sxs-lookup"><span data-stu-id="02d64-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="02d64-128">Por padrão, **set-AzureSubscription** usa o arquivo de dados de assinatura padrão em seu perfil de usuário móvel.</span><span class="sxs-lookup"><span data-stu-id="02d64-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="02d64-129">OS</span><span class="sxs-lookup"><span data-stu-id="02d64-129">PARAMETERS</span></span>

### <span data-ttu-id="02d64-130">-Certificado</span><span class="sxs-lookup"><span data-stu-id="02d64-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d64-131">-Contexto</span><span class="sxs-lookup"><span data-stu-id="02d64-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d64-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02d64-132">-CurrentStorageAccountName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d64-133">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="02d64-133">-Environment</span></span>
<span data-ttu-id="02d64-134">Especifica um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="02d64-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="02d64-135">Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.</span><span class="sxs-lookup"><span data-stu-id="02d64-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="02d64-136">Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.</span><span class="sxs-lookup"><span data-stu-id="02d64-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="02d64-137">Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="02d64-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d64-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02d64-138">-PassThru</span></span>
<span data-ttu-id="02d64-139">Retorna $True se o comando tiver êxito e $False se falhar.</span><span class="sxs-lookup"><span data-stu-id="02d64-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="02d64-140">Por padrão, esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="02d64-140">By default, this cmdlet does not return any output.</span></span>
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

### <span data-ttu-id="02d64-141">-Perfil</span><span class="sxs-lookup"><span data-stu-id="02d64-141">-Profile</span></span>
<span data-ttu-id="02d64-142">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="02d64-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="02d64-143">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="02d64-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02d64-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="02d64-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="02d64-145">Especifica o ponto de extremidade dos dados do Azure Resource Manager, incluindo dados sobre grupos de recursos associados à conta.</span><span class="sxs-lookup"><span data-stu-id="02d64-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="02d64-146">Para obter mais informações sobre o Azure Resource Manager, consulte [cmdlets do Azure Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) e [uso do Windows PowerShell com o Gerenciador de recursos](https://go.microsoft.com/fwlink/?LinkID=394767) https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="02d64-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="02d64-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="02d64-147">-ServiceEndpoint</span></span>
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

### <span data-ttu-id="02d64-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02d64-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d64-149">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="02d64-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d64-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d64-150">CommonParameters</span></span>
<span data-ttu-id="02d64-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d64-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d64-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d64-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d64-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02d64-153">INPUTS</span></span>

### <span data-ttu-id="02d64-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="02d64-154">None</span></span>
<span data-ttu-id="02d64-155">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="02d64-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="02d64-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02d64-156">OUTPUTS</span></span>

### <span data-ttu-id="02d64-157">None ou System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02d64-157">None or System.Boolean</span></span>
<span data-ttu-id="02d64-158">Quando você usa o parâmetro *PassThru* , esse cmdlet retorna um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="02d64-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="02d64-159">Por padrão, esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="02d64-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="02d64-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02d64-160">NOTES</span></span>

## <span data-ttu-id="02d64-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02d64-161">RELATED LINKS</span></span>

[<span data-ttu-id="02d64-162">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="02d64-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="02d64-163">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="02d64-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="02d64-164">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="02d64-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="02d64-165">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="02d64-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="02d64-166">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="02d64-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


