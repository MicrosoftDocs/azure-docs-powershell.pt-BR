---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 7e746e7d67672a57e3e8aa257a4e3dfbe3b51054
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602483"
---
# <span data-ttu-id="6574a-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6574a-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="6574a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6574a-102">SYNOPSIS</span></span>
<span data-ttu-id="6574a-103">Cria um novo perfil de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="6574a-103">Creates a new activity log profile.</span></span> <span data-ttu-id="6574a-104">Esse perfil é usado para arquivar o log de atividades em uma conta de armazenamento do Azure ou transmiti-lo para um hub de eventos do Azure na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6574a-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6574a-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6574a-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6574a-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6574a-106">DESCRIPTION</span></span>
<span data-ttu-id="6574a-107">O cmdlet **Add-AzureRmLogProfile** cria um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="6574a-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="6574a-108">**Conta de armazenamento** somente conta de armazenamento padrão (conta de armazenamento Premium não é suportada) é suportada.</span><span class="sxs-lookup"><span data-stu-id="6574a-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="6574a-109">Ele pode ser do tipo ARM ou Classic.</span><span class="sxs-lookup"><span data-stu-id="6574a-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="6574a-110">Se estiver conectado a uma conta de armazenamento, o custo de armazenamento do log de atividades será cobrado em tarifas normais de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="6574a-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="6574a-111">Pode haver apenas um perfil de log por assinatura com apenas uma conta de armazenamento por assinatura pode ser usada para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="6574a-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="6574a-112">**Hub de eventos** – pode haver apenas um perfil de log por assinatura que apenas um hub de eventos por assinatura pode ser usado para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="6574a-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="6574a-113">Se o log de atividades for transmitido para um hub de eventos, será aplicado o preço padrão do Hub do evento.</span><span class="sxs-lookup"><span data-stu-id="6574a-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="6574a-114">No log de atividades, os eventos podem pertencer a uma região ou podem ser "global".</span><span class="sxs-lookup"><span data-stu-id="6574a-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="6574a-115">Basicamente, o global significa que esses eventos são independentes de região e são independentes da região, na verdade, a maioria dos eventos se encaixa nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="6574a-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="6574a-116">Se o perfil do log de atividades for definido no portal, ele adicionará implicitamente "global" juntamente com qualquer outra região selecionada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6574a-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="6574a-117">Ao usar o cmdlet, o local como "global" deve ser explicitamente mencionado separadamente de qualquer outra região.</span><span class="sxs-lookup"><span data-stu-id="6574a-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="6574a-118">**Observação** :- **falha ao definir "global" nos locais resultará na maioria dos registros de atividades não exportados.**</span><span class="sxs-lookup"><span data-stu-id="6574a-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="6574a-119">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="6574a-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="6574a-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6574a-120">EXAMPLES</span></span>

### <span data-ttu-id="6574a-121">Exemplo 1: adicionar um novo perfil de log para exportar o log de atividades correspondente à condição de localização para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6574a-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="6574a-122">OS</span><span class="sxs-lookup"><span data-stu-id="6574a-122">PARAMETERS</span></span>

### <span data-ttu-id="6574a-123">-Categoria</span><span class="sxs-lookup"><span data-stu-id="6574a-123">-Category</span></span>
<span data-ttu-id="6574a-124">Especifica a lista de categorias.</span><span class="sxs-lookup"><span data-stu-id="6574a-124">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="6574a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6574a-125">-DefaultProfile</span></span>
<span data-ttu-id="6574a-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6574a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6574a-127">-Local</span><span class="sxs-lookup"><span data-stu-id="6574a-127">-Location</span></span>
<span data-ttu-id="6574a-128">Especifica o local do perfil de log.</span><span class="sxs-lookup"><span data-stu-id="6574a-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="6574a-129">Valores válidos: execute abaixo o cmdlet para obter a lista de locais mais recente.</span><span class="sxs-lookup"><span data-stu-id="6574a-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="6574a-130">Get-AzureLocation | Selecionar DisplayName</span><span class="sxs-lookup"><span data-stu-id="6574a-130">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="6574a-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="6574a-131">-Name</span></span>
<span data-ttu-id="6574a-132">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="6574a-132">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="6574a-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6574a-133">-RetentionInDays</span></span>
<span data-ttu-id="6574a-134">Especifica a política de retenção, em dias.</span><span class="sxs-lookup"><span data-stu-id="6574a-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="6574a-135">Este é o número de dias durante os quais os logs são preservados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="6574a-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="6574a-136">Para reter os dados para sempre, defina-o como **0**.</span><span class="sxs-lookup"><span data-stu-id="6574a-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="6574a-137">Se não for especificado, o padrão será **0**.</span><span class="sxs-lookup"><span data-stu-id="6574a-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="6574a-138">O armazenamento padrão normal ou as tarifas de cobrança do hub de eventos serão aplicadas para a retenção de dados.</span><span class="sxs-lookup"><span data-stu-id="6574a-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="6574a-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="6574a-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="6574a-140">Especifica a ID da regra de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="6574a-140">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="6574a-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6574a-141">-StorageAccountId</span></span>
<span data-ttu-id="6574a-142">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6574a-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="6574a-143">ID é a ID do recurso totalmente qualificado da conta de armazenamento, por exemplo</span><span class="sxs-lookup"><span data-stu-id="6574a-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="6574a-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="6574a-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="6574a-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6574a-145">-Confirm</span></span>
<span data-ttu-id="6574a-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6574a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6574a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6574a-147">-WhatIf</span></span>
<span data-ttu-id="6574a-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6574a-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6574a-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6574a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6574a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6574a-150">CommonParameters</span></span>
<span data-ttu-id="6574a-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6574a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6574a-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6574a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6574a-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6574a-153">INPUTS</span></span>

### <span data-ttu-id="6574a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="6574a-154">System.String</span></span>

### <span data-ttu-id="6574a-155">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6574a-155">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6574a-156">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6574a-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6574a-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6574a-157">OUTPUTS</span></span>

### <span data-ttu-id="6574a-158">Microsoft. Azure. Commands. insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="6574a-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="6574a-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6574a-159">NOTES</span></span>

## <span data-ttu-id="6574a-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6574a-160">RELATED LINKS</span></span>

[<span data-ttu-id="6574a-161">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6574a-161">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="6574a-162">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6574a-162">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


