---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112963"
---
# <span data-ttu-id="091d9-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="091d9-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="091d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="091d9-102">SYNOPSIS</span></span>
<span data-ttu-id="091d9-103">Cria um novo perfil de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="091d9-103">Creates a new activity log profile.</span></span> <span data-ttu-id="091d9-104">Esse perfil é usado para arquivar o log de atividades em uma conta de armazenamento do Azure ou para transmitir para um hub de eventos do Azure na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="091d9-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="091d9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="091d9-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="091d9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="091d9-106">DESCRIPTION</span></span>
<span data-ttu-id="091d9-107">O **cmdlet Add-AzLogProfile** cria um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="091d9-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="091d9-108">**Conta de Armazenamento** – Somente a conta de armazenamento padrão (não há suporte para conta de armazenamento premium) é suportada.</span><span class="sxs-lookup"><span data-stu-id="091d9-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="091d9-109">Pode ser do tipo ARM ou Clássico.</span><span class="sxs-lookup"><span data-stu-id="091d9-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="091d9-110">Se ele estiver conectado a uma conta de armazenamento, o custo de armazenar o log de atividades será cobrado com taxas de armazenamento padrão normais.</span><span class="sxs-lookup"><span data-stu-id="091d9-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="091d9-111">Pode haver apenas um perfil de log por assinatura, consequentemente, apenas uma conta de armazenamento por assinatura pode ser usada para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="091d9-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="091d9-112">**Hub de Eventos** – pode haver apenas um perfil de log por assinatura, consequentemente, somente um hub de evento por assinatura pode ser usado para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="091d9-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="091d9-113">Se o log de atividades for transmitido para um hub de eventos, o preço padrão do hub de eventos será aplicado.</span><span class="sxs-lookup"><span data-stu-id="091d9-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="091d9-114">No log de atividades, os eventos podem pertencer a uma região ou podem ser "Globais".</span><span class="sxs-lookup"><span data-stu-id="091d9-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="091d9-115">Global essencialmente significa que esses eventos são agnéticos de região e são independentes da região, na verdade a maioria dos eventos se enquadram nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="091d9-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="091d9-116">Se o perfil do log de atividades estiver definido a partir do portal, ele adiciona implicitamente "Global" juntamente com qualquer outra região selecionada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="091d9-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="091d9-117">Ao usar o cmdlet, o local como "Global" deve ser explicitamente mencionado além de qualquer outra região.</span><span class="sxs-lookup"><span data-stu-id="091d9-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="091d9-118">**Observação** :- **Não definir "Global"** nos locais resultará em uma maioria do log de atividades não sendo exportado.</span><span class="sxs-lookup"><span data-stu-id="091d9-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="091d9-119">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="091d9-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="091d9-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="091d9-120">EXAMPLES</span></span>

### <span data-ttu-id="091d9-121">Exemplo 1: Adicionar um novo perfil de log para exportar o log de atividades que corresponde a condição de local a uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="091d9-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="091d9-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="091d9-122">Example 2</span></span>

<span data-ttu-id="091d9-123">Cria um novo perfil de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="091d9-123">Creates a new activity log profile.</span></span> <span data-ttu-id="091d9-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="091d9-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="091d9-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="091d9-125">PARAMETERS</span></span>

### <span data-ttu-id="091d9-126">-Categoria</span><span class="sxs-lookup"><span data-stu-id="091d9-126">-Category</span></span>
<span data-ttu-id="091d9-127">Especifica a lista de categorias.</span><span class="sxs-lookup"><span data-stu-id="091d9-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="091d9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="091d9-128">-DefaultProfile</span></span>
<span data-ttu-id="091d9-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="091d9-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="091d9-130">-Local</span><span class="sxs-lookup"><span data-stu-id="091d9-130">-Location</span></span>
<span data-ttu-id="091d9-131">Especifica o local do perfil de log.</span><span class="sxs-lookup"><span data-stu-id="091d9-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="091d9-132">Valores válidos: Execute abaixo do cmdlet para obter a lista de locais mais recente.</span><span class="sxs-lookup"><span data-stu-id="091d9-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="091d9-133">Get-AzLocation | Selecionar Nome de Exibição</span><span class="sxs-lookup"><span data-stu-id="091d9-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="091d9-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="091d9-134">-Name</span></span>
<span data-ttu-id="091d9-135">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="091d9-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="091d9-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="091d9-136">-RetentionInDays</span></span>
<span data-ttu-id="091d9-137">Especifica a política de retenção em dias.</span><span class="sxs-lookup"><span data-stu-id="091d9-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="091d9-138">Esse é o número de dias em que os logs são preservados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="091d9-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="091d9-139">Para manter os dados definidos para sempre como **0.**</span><span class="sxs-lookup"><span data-stu-id="091d9-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="091d9-140">Se não for especificado, ele será padrão para **0.**</span><span class="sxs-lookup"><span data-stu-id="091d9-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="091d9-141">As taxas de cobrança do hub de eventos ou armazenamento padrão normal serão aplicadas à retenção de dados.</span><span class="sxs-lookup"><span data-stu-id="091d9-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="091d9-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="091d9-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="091d9-143">Especifica a ID da regra de Barra de Serviço.</span><span class="sxs-lookup"><span data-stu-id="091d9-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="091d9-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="091d9-144">-StorageAccountId</span></span>
<span data-ttu-id="091d9-145">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="091d9-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="091d9-146">A ID é a ID de Recurso totalmente qualificada da conta de armazenamento, por exemplo</span><span class="sxs-lookup"><span data-stu-id="091d9-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="091d9-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="091d9-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="091d9-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="091d9-148">-Confirm</span></span>
<span data-ttu-id="091d9-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="091d9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="091d9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="091d9-150">-WhatIf</span></span>
<span data-ttu-id="091d9-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="091d9-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="091d9-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="091d9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="091d9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091d9-153">CommonParameters</span></span>
<span data-ttu-id="091d9-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="091d9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091d9-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="091d9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091d9-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="091d9-156">INPUTS</span></span>

### <span data-ttu-id="091d9-157">System.String</span><span class="sxs-lookup"><span data-stu-id="091d9-157">System.String</span></span>

### <span data-ttu-id="091d9-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="091d9-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="091d9-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="091d9-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="091d9-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="091d9-160">OUTPUTS</span></span>

### <span data-ttu-id="091d9-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="091d9-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="091d9-162">Notas</span><span class="sxs-lookup"><span data-stu-id="091d9-162">NOTES</span></span>

## <span data-ttu-id="091d9-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="091d9-163">RELATED LINKS</span></span>

[<span data-ttu-id="091d9-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="091d9-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="091d9-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="091d9-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


