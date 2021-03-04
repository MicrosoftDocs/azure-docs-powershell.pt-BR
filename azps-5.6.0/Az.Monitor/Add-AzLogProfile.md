---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888926"
---
# <span data-ttu-id="45d35-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="45d35-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="45d35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d35-102">SYNOPSIS</span></span>
<span data-ttu-id="45d35-103">Cria um novo perfil de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45d35-103">Creates a new activity log profile.</span></span> <span data-ttu-id="45d35-104">Esse perfil é usado para arquivar o log de atividades em uma conta de armazenamento do Azure ou para transmitir para um hub de eventos do Azure na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="45d35-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="45d35-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45d35-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d35-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45d35-106">DESCRIPTION</span></span>
<span data-ttu-id="45d35-107">O cmdlet **Add-AzLogProfile** cria um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="45d35-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="45d35-108">**Conta de** Armazenamento - Somente conta de armazenamento padrão (conta de armazenamento premium não é suportada) é suportada.</span><span class="sxs-lookup"><span data-stu-id="45d35-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="45d35-109">Pode ser do tipo ARM ou Clássico.</span><span class="sxs-lookup"><span data-stu-id="45d35-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="45d35-110">Se ele estiver conectado a uma conta de armazenamento, o custo de armazenar o log de atividades será cobrado com taxas de armazenamento padrão normais.</span><span class="sxs-lookup"><span data-stu-id="45d35-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="45d35-111">Pode haver apenas um perfil de log por assinatura, consequentemente, apenas uma conta de armazenamento por assinatura pode ser usada para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45d35-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="45d35-112">**Hub de Eventos** - Pode haver apenas um perfil de log por assinatura, consequentemente, apenas um hub de eventos por assinatura pode ser usado para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45d35-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="45d35-113">Se o log de atividades for transmitido para um hub de eventos, o preço padrão do hub de eventos será aplicado.</span><span class="sxs-lookup"><span data-stu-id="45d35-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="45d35-114">No log de atividades, os eventos podem pertencer a uma região ou podem ser "Globais".</span><span class="sxs-lookup"><span data-stu-id="45d35-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="45d35-115">Global essencialmente significa que esses eventos são agnósticos de região e são independentes da região, na verdade, a maioria dos eventos se enquadra nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="45d35-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="45d35-116">Se o perfil do log de atividades for definido a partir do portal, ele adiciona implicitamente "Global" juntamente com qualquer outra região selecionada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="45d35-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="45d35-117">Ao usar o cmdlet, o local como "Global" deve ser explicitamente mencionado além de qualquer outra região.</span><span class="sxs-lookup"><span data-stu-id="45d35-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="45d35-118">**Observação** :- **Falha ao definir "Global"** nos locais resultará em uma maioria do log de atividades não sendo exportado.</span><span class="sxs-lookup"><span data-stu-id="45d35-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="45d35-119">Este cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="45d35-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="45d35-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45d35-120">EXAMPLES</span></span>

### <span data-ttu-id="45d35-121">Exemplo 1: Adicionar um novo perfil de log para exportar o log de atividades que corresponde à condição de local para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="45d35-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="45d35-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="45d35-122">Example 2</span></span>

<span data-ttu-id="45d35-123">Cria um novo perfil de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45d35-123">Creates a new activity log profile.</span></span> <span data-ttu-id="45d35-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="45d35-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="45d35-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45d35-125">PARAMETERS</span></span>

### <span data-ttu-id="45d35-126">-Category</span><span class="sxs-lookup"><span data-stu-id="45d35-126">-Category</span></span>
<span data-ttu-id="45d35-127">Especifica a lista de categorias.</span><span class="sxs-lookup"><span data-stu-id="45d35-127">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d35-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d35-128">-DefaultProfile</span></span>
<span data-ttu-id="45d35-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="45d35-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d35-130">-Location</span><span class="sxs-lookup"><span data-stu-id="45d35-130">-Location</span></span>
<span data-ttu-id="45d35-131">Especifica o local do perfil de log.</span><span class="sxs-lookup"><span data-stu-id="45d35-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="45d35-132">Valores válidos: Execute abaixo do cmdlet para obter a lista mais recente de locais.</span><span class="sxs-lookup"><span data-stu-id="45d35-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="45d35-133">Get-AzLocation | Selecionar DisplayName</span><span class="sxs-lookup"><span data-stu-id="45d35-133">Get-AzLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d35-134">-Name</span><span class="sxs-lookup"><span data-stu-id="45d35-134">-Name</span></span>
<span data-ttu-id="45d35-135">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="45d35-135">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d35-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="45d35-136">-RetentionInDays</span></span>
<span data-ttu-id="45d35-137">Especifica a política de retenção, em dias.</span><span class="sxs-lookup"><span data-stu-id="45d35-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="45d35-138">Esse é o número de dias em que os logs são preservados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="45d35-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="45d35-139">Para manter os dados definidos para sempre como **0**.</span><span class="sxs-lookup"><span data-stu-id="45d35-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="45d35-140">Se não for especificado, o padrão é **0**.</span><span class="sxs-lookup"><span data-stu-id="45d35-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="45d35-141">As taxas de cobrança padrão de armazenamento ou hub de eventos serão aplicadas para retenção de dados.</span><span class="sxs-lookup"><span data-stu-id="45d35-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d35-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="45d35-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="45d35-143">Especifica a ID da regra de Barramento de Serviço.</span><span class="sxs-lookup"><span data-stu-id="45d35-143">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d35-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="45d35-144">-StorageAccountId</span></span>
<span data-ttu-id="45d35-145">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="45d35-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="45d35-146">ID é a ID de Recurso totalmente qualificada da conta de armazenamento, por exemplo</span><span class="sxs-lookup"><span data-stu-id="45d35-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="45d35-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="45d35-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d35-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45d35-148">-Confirm</span></span>
<span data-ttu-id="45d35-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45d35-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d35-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d35-150">-WhatIf</span></span>
<span data-ttu-id="45d35-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45d35-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45d35-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45d35-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d35-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d35-153">CommonParameters</span></span>
<span data-ttu-id="45d35-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d35-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d35-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45d35-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d35-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45d35-156">INPUTS</span></span>

### <span data-ttu-id="45d35-157">System.String</span><span class="sxs-lookup"><span data-stu-id="45d35-157">System.String</span></span>

### <span data-ttu-id="45d35-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="45d35-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="45d35-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="45d35-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="45d35-160">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45d35-160">OUTPUTS</span></span>

### <span data-ttu-id="45d35-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="45d35-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="45d35-162">NOTES</span><span class="sxs-lookup"><span data-stu-id="45d35-162">NOTES</span></span>

## <span data-ttu-id="45d35-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45d35-163">RELATED LINKS</span></span>

[<span data-ttu-id="45d35-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="45d35-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="45d35-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="45d35-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


