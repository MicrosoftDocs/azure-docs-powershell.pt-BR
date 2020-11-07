---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946274"
---
# <span data-ttu-id="38d8d-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="38d8d-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="38d8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="38d8d-103">Obtém os sites do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="38d8d-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="38d8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38d8d-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="38d8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="38d8d-106">O cmdlet **Get-AzureWebsite** Obtém informações sobre os sites do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="38d8d-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="38d8d-107">Por padrão, **Get-AzureWebsite** Obtém todos os websites do Azure na assinatura atual e retorna um objeto que fornece informações básicas sobre os sites.</span><span class="sxs-lookup"><span data-stu-id="38d8d-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="38d8d-108">Quando você usa o parâmetro *Name* , **Get-AzureWebsite** retorna um objeto com informações abrangentes, incluindo detalhes de configuração.</span><span class="sxs-lookup"><span data-stu-id="38d8d-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="38d8d-109">A assinatura atual é a assinatura designada como "atual".</span><span class="sxs-lookup"><span data-stu-id="38d8d-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="38d8d-110">Para localizar a assinatura atual, use o parâmetro *atual* do cmdlet [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .</span><span class="sxs-lookup"><span data-stu-id="38d8d-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="38d8d-111">Para alterar a assinatura atual, use o cmdlet [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .</span><span class="sxs-lookup"><span data-stu-id="38d8d-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="38d8d-112">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38d8d-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="38d8d-113">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="38d8d-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="38d8d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38d8d-114">EXAMPLES</span></span>

### <span data-ttu-id="38d8d-115">Exemplo 1: obter todos os sites na assinatura</span><span class="sxs-lookup"><span data-stu-id="38d8d-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="38d8d-116">Este comando obtém todos os websites do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="38d8d-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="38d8d-117">Exemplo 2: obter um site por nome</span><span class="sxs-lookup"><span data-stu-id="38d8d-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="38d8d-118">Esse comando obtém informações detalhadas sobre o site do Azure ContosoWeb, incluindo informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="38d8d-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="38d8d-119">Quando você usa o parâmetro *Name* , **Get-AzureWebsite** retorna um objeto **SiteWithConfig** com informações estendidas sobre o site.</span><span class="sxs-lookup"><span data-stu-id="38d8d-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="38d8d-120">Exemplo 3: obter informações detalhadas sobre todos os sites</span><span class="sxs-lookup"><span data-stu-id="38d8d-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="38d8d-121">Este comando obtém informações detalhadas sobre todos os sites na assinatura.</span><span class="sxs-lookup"><span data-stu-id="38d8d-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="38d8d-122">Ele usa um comando **Get-AzureWebsite** para obter todos os sites e, em seguida, usa o cmdlet **ForEach-Object** para obter cada site por nome.</span><span class="sxs-lookup"><span data-stu-id="38d8d-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="38d8d-123">Exemplo 4: obter informações sobre um slot de implantação</span><span class="sxs-lookup"><span data-stu-id="38d8d-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="38d8d-124">Esse comando obtém o slot de implantação de preparo do site do ContosoWeb.</span><span class="sxs-lookup"><span data-stu-id="38d8d-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="38d8d-125">Os slots de implantação permitem testar versões diferentes do seu site do Azure sem liberá-los para o público.</span><span class="sxs-lookup"><span data-stu-id="38d8d-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="38d8d-126">Exemplo 5: obter instâncias de site</span><span class="sxs-lookup"><span data-stu-id="38d8d-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="38d8d-127">Os comandos neste exemplo usam a propriedade instances de um site do Azure para obter informações sobre instâncias de sites em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="38d8d-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="38d8d-128">A propriedade **Instances** foi adicionada ao objeto **SiteWithConfig** na versão 0.8.3 do módulo do Azure.</span><span class="sxs-lookup"><span data-stu-id="38d8d-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="38d8d-129">O primeiro comando obtém as IDs de instância de todas as instâncias atualmente em execução de um site.</span><span class="sxs-lookup"><span data-stu-id="38d8d-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="38d8d-130">O segundo comando obtém o número de instâncias em execução do site.</span><span class="sxs-lookup"><span data-stu-id="38d8d-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="38d8d-131">Você pode usar a propriedade **Count** em qualquer matriz.</span><span class="sxs-lookup"><span data-stu-id="38d8d-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="38d8d-132">OS</span><span class="sxs-lookup"><span data-stu-id="38d8d-132">PARAMETERS</span></span>

### <span data-ttu-id="38d8d-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="38d8d-133">-Name</span></span>
<span data-ttu-id="38d8d-134">Obtém informações de configuração detalhadas sobre o site especificado.</span><span class="sxs-lookup"><span data-stu-id="38d8d-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="38d8d-135">Digite o nome de um site na assinatura.</span><span class="sxs-lookup"><span data-stu-id="38d8d-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="38d8d-136">Por padrão, **Get-AzureWebsite** Obtém todos os sites na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="38d8d-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="38d8d-137">O valor de *nome* não oferece suporte a caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="38d8d-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="38d8d-138">-Perfil</span><span class="sxs-lookup"><span data-stu-id="38d8d-138">-Profile</span></span>
<span data-ttu-id="38d8d-139">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="38d8d-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38d8d-140">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="38d8d-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38d8d-141">-Slot</span><span class="sxs-lookup"><span data-stu-id="38d8d-141">-Slot</span></span>
<span data-ttu-id="38d8d-142">Obtém o slot de implantação especificado do site.</span><span class="sxs-lookup"><span data-stu-id="38d8d-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="38d8d-143">Digite o nome do slot, como "preparação" ou "produção".</span><span class="sxs-lookup"><span data-stu-id="38d8d-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="38d8d-144">Para obter mais informações sobre slots de implantação, consulte implantação em estágios em sites do Microsoft Azure https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .</span><span class="sxs-lookup"><span data-stu-id="38d8d-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="38d8d-145">Para adicionar um slot de implantação a um site do Azure existente, use o cmdlet Set-AzureWebsite.</span><span class="sxs-lookup"><span data-stu-id="38d8d-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="38d8d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d8d-146">CommonParameters</span></span>
<span data-ttu-id="38d8d-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d8d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d8d-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d8d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d8d-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38d8d-149">INPUTS</span></span>

### <span data-ttu-id="38d8d-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="38d8d-150">None</span></span>
<span data-ttu-id="38d8d-151">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="38d8d-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="38d8d-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38d8d-152">OUTPUTS</span></span>

### <span data-ttu-id="38d8d-153">Microsoft. WindowsAzure. Commands. Utilities. sites. Services. webentities. site</span><span class="sxs-lookup"><span data-stu-id="38d8d-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="38d8d-154">Por padrão, **Get-AzureWebsite** retorna uma matriz de objetos do **site** .</span><span class="sxs-lookup"><span data-stu-id="38d8d-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="38d8d-155">Microsoft. WindowsAzure. Commands. Utilities. sites. Services. webentities. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="38d8d-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="38d8d-156">Quando você usa o parâmetro *Name* , **Get-AzureWebsite** retorna um objeto **SiteWithConfig** .</span><span class="sxs-lookup"><span data-stu-id="38d8d-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="38d8d-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38d8d-157">NOTES</span></span>

## <span data-ttu-id="38d8d-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38d8d-158">RELATED LINKS</span></span>

[<span data-ttu-id="38d8d-159">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="38d8d-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="38d8d-160">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="38d8d-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="38d8d-161">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="38d8d-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="38d8d-162">Parar-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="38d8d-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="38d8d-163">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="38d8d-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


