---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: beef1ab92a931f4f4041d9e9083712fe0b14f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770349"
---
# <span data-ttu-id="fb0ec-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="fb0ec-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="fb0ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fb0ec-103">Cria um novo perfil de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-103">Creates a new activity log profile.</span></span> <span data-ttu-id="fb0ec-104">Esse perfil é usado para arquivar o log de atividades em uma conta de armazenamento do Azure ou transmiti-lo para um hub de eventos do Azure na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="fb0ec-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb0ec-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb0ec-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb0ec-106">DESCRIPTION</span></span>
<span data-ttu-id="fb0ec-107">O cmdlet **Add-AzLogProfile** cria um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="fb0ec-108">**Conta de armazenamento** somente conta de armazenamento padrão (conta de armazenamento Premium não é suportada) é suportada.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="fb0ec-109">Ele pode ser do tipo ARM ou Classic.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="fb0ec-110">Se estiver conectado a uma conta de armazenamento, o custo de armazenamento do log de atividades será cobrado em tarifas normais de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="fb0ec-111">Pode haver apenas um perfil de log por assinatura com apenas uma conta de armazenamento por assinatura pode ser usada para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="fb0ec-112">**Hub de eventos** – pode haver apenas um perfil de log por assinatura que apenas um hub de eventos por assinatura pode ser usado para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="fb0ec-113">Se o log de atividades for transmitido para um hub de eventos, será aplicado o preço padrão do Hub do evento.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="fb0ec-114">No log de atividades, os eventos podem pertencer a uma região ou podem ser "global".</span><span class="sxs-lookup"><span data-stu-id="fb0ec-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="fb0ec-115">Basicamente, o global significa que esses eventos são independentes de região e são independentes da região, na verdade, a maioria dos eventos se encaixa nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="fb0ec-116">Se o perfil do log de atividades for definido no portal, ele adicionará implicitamente "global" juntamente com qualquer outra região selecionada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="fb0ec-117">Ao usar o cmdlet, o local como "global" deve ser explicitamente mencionado separadamente de qualquer outra região.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="fb0ec-118">**Observação** :- **falha ao definir "global" nos locais resultará na maioria dos registros de atividades não exportados.**</span><span class="sxs-lookup"><span data-stu-id="fb0ec-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="fb0ec-119">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="fb0ec-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb0ec-120">EXAMPLES</span></span>

### <span data-ttu-id="fb0ec-121">Exemplo 1: adicionar um novo perfil de log para exportar o log de atividades correspondente à condição de localização para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fb0ec-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="fb0ec-122">OS</span><span class="sxs-lookup"><span data-stu-id="fb0ec-122">PARAMETERS</span></span>

### <span data-ttu-id="fb0ec-123">-Categoria</span><span class="sxs-lookup"><span data-stu-id="fb0ec-123">-Category</span></span>
<span data-ttu-id="fb0ec-124">Especifica a lista de categorias.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-124">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="fb0ec-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb0ec-125">-DefaultProfile</span></span>
<span data-ttu-id="fb0ec-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fb0ec-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb0ec-127">-Local</span><span class="sxs-lookup"><span data-stu-id="fb0ec-127">-Location</span></span>
<span data-ttu-id="fb0ec-128">Especifica o local do perfil de log.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="fb0ec-129">Valores válidos: execute abaixo o cmdlet para obter a lista de locais mais recente.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="fb0ec-130">Get-AzLocation | Selecionar DisplayName</span><span class="sxs-lookup"><span data-stu-id="fb0ec-130">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="fb0ec-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb0ec-131">-Name</span></span>
<span data-ttu-id="fb0ec-132">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-132">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="fb0ec-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fb0ec-133">-RetentionInDays</span></span>
<span data-ttu-id="fb0ec-134">Especifica a política de retenção, em dias.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="fb0ec-135">Este é o número de dias durante os quais os logs são preservados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="fb0ec-136">Para reter os dados para sempre, defina-o como **0**.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="fb0ec-137">Se não for especificado, o padrão será **0**.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="fb0ec-138">O armazenamento padrão normal ou as tarifas de cobrança do hub de eventos serão aplicadas para a retenção de dados.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="fb0ec-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="fb0ec-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="fb0ec-140">Especifica a ID da regra de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-140">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="fb0ec-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fb0ec-141">-StorageAccountId</span></span>
<span data-ttu-id="fb0ec-142">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="fb0ec-143">ID é a ID do recurso totalmente qualificado da conta de armazenamento, por exemplo</span><span class="sxs-lookup"><span data-stu-id="fb0ec-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="fb0ec-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="fb0ec-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="fb0ec-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb0ec-145">-Confirm</span></span>
<span data-ttu-id="fb0ec-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb0ec-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb0ec-147">-WhatIf</span></span>
<span data-ttu-id="fb0ec-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb0ec-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb0ec-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0ec-150">CommonParameters</span></span>
<span data-ttu-id="fb0ec-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb0ec-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0ec-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb0ec-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0ec-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb0ec-153">INPUTS</span></span>

### <span data-ttu-id="fb0ec-154">System. String</span><span class="sxs-lookup"><span data-stu-id="fb0ec-154">System.String</span></span>

### <span data-ttu-id="fb0ec-155">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb0ec-155">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb0ec-156">System. Collections. Generic. List ' 1 [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb0ec-156">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fb0ec-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb0ec-157">OUTPUTS</span></span>

### <span data-ttu-id="fb0ec-158">Microsoft. Azure. Commands. insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="fb0ec-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="fb0ec-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb0ec-159">NOTES</span></span>

## <span data-ttu-id="fb0ec-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb0ec-160">RELATED LINKS</span></span>

[<span data-ttu-id="fb0ec-161">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="fb0ec-161">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="fb0ec-162">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="fb0ec-162">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


