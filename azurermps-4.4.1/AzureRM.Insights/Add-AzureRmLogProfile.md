---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441058"
---
# <span data-ttu-id="8e73e-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e73e-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="8e73e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e73e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e73e-103">Cria um novo perfil de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="8e73e-103">Creates a new activity log profile.</span></span> <span data-ttu-id="8e73e-104">Esse perfil é usado para arquivar o log de atividades em uma conta de armazenamento do Azure ou transmiti-lo para um hub de eventos do Azure na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="8e73e-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="8e73e-105">**Conta de armazenamento** somente conta de armazenamento padrão (conta de armazenamento Premium não é suportada) é suportada.</span><span class="sxs-lookup"><span data-stu-id="8e73e-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="8e73e-106">Ele pode ser do tipo ARM ou Classic.</span><span class="sxs-lookup"><span data-stu-id="8e73e-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="8e73e-107">Se estiver conectado a uma conta de armazenamento, o custo de armazenamento do log de atividades será cobrado em tarifas normais de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="8e73e-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="8e73e-108">Pode haver apenas um perfil de log por assinatura com apenas uma conta de armazenamento por assinatura pode ser usada para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="8e73e-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="8e73e-109">**Hub de eventos** – pode haver apenas um perfil de log por assinatura que apenas um hub de eventos por assinatura pode ser usado para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="8e73e-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="8e73e-110">Se o log de atividades for transmitido para um hub de eventos, será aplicado o preço padrão do Hub do evento.</span><span class="sxs-lookup"><span data-stu-id="8e73e-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="8e73e-111">No log de atividades, os eventos podem pertencer a uma região ou podem ser "global".</span><span class="sxs-lookup"><span data-stu-id="8e73e-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="8e73e-112">Basicamente, o global significa que esses eventos são independentes de região e são independentes da região, na verdade, a maioria dos eventos se encaixa nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="8e73e-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="8e73e-113">Se o perfil do log de atividades for definido no portal, ele adicionará implicitamente "global" juntamente com qualquer outra região selecionada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8e73e-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="8e73e-114">Ao usar o cmdlet, o local como "global" deve ser explicitamente mencionado separadamente de qualquer outra região.</span><span class="sxs-lookup"><span data-stu-id="8e73e-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="8e73e-115">**Observação** :- **falha ao definir "global" nos locais resultará na maioria dos registros de atividades não exportados.**</span><span class="sxs-lookup"><span data-stu-id="8e73e-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e73e-116">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e73e-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e73e-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e73e-117">DESCRIPTION</span></span>
<span data-ttu-id="8e73e-118">O cmdlet **Add-AzureRmLogProfile** cria um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="8e73e-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="8e73e-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e73e-119">EXAMPLES</span></span>

### <span data-ttu-id="8e73e-120">Exemplo 1: adicionar um novo perfil de log para exportar o log de atividades correspondente à condição de localização para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8e73e-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="8e73e-121">OS</span><span class="sxs-lookup"><span data-stu-id="8e73e-121">PARAMETERS</span></span>

### <span data-ttu-id="8e73e-122">-Categorias</span><span class="sxs-lookup"><span data-stu-id="8e73e-122">-Categories</span></span>
<span data-ttu-id="8e73e-123">Especifica a lista de categorias.</span><span class="sxs-lookup"><span data-stu-id="8e73e-123">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="8e73e-124">-Localizações</span><span class="sxs-lookup"><span data-stu-id="8e73e-124">-Locations</span></span>
<span data-ttu-id="8e73e-125">Especifica o local do perfil de log.</span><span class="sxs-lookup"><span data-stu-id="8e73e-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="8e73e-126">Valores válidos: execute abaixo o cmdlet para obter a lista de locais mais recente.</span><span class="sxs-lookup"><span data-stu-id="8e73e-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="8e73e-127">Get-AzureLocation | Selecionar DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e73e-127">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="8e73e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e73e-128">-Name</span></span>
<span data-ttu-id="8e73e-129">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="8e73e-129">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="8e73e-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8e73e-130">-RetentionInDays</span></span>
<span data-ttu-id="8e73e-131">Especifica a política de retenção, em dias.</span><span class="sxs-lookup"><span data-stu-id="8e73e-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="8e73e-132">Este é o número de dias durante os quais os logs são preservados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="8e73e-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="8e73e-133">Para reter os dados para sempre, defina-o como **0**.</span><span class="sxs-lookup"><span data-stu-id="8e73e-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="8e73e-134">Se não for especificado, o padrão será **0**.</span><span class="sxs-lookup"><span data-stu-id="8e73e-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="8e73e-135">O armazenamento padrão normal ou as tarifas de cobrança do hub de eventos serão aplicadas para a retenção de dados.</span><span class="sxs-lookup"><span data-stu-id="8e73e-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="8e73e-136">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="8e73e-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="8e73e-137">Especifica a ID da regra de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="8e73e-137">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="8e73e-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e73e-138">-StorageAccountId</span></span>
<span data-ttu-id="8e73e-139">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e73e-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="8e73e-140">ID é a ID do recurso totalmente qualificado da conta de armazenamento, por exemplo</span><span class="sxs-lookup"><span data-stu-id="8e73e-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="8e73e-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="8e73e-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="8e73e-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e73e-142">-DefaultProfile</span></span>
<span data-ttu-id="8e73e-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e73e-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e73e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e73e-144">CommonParameters</span></span>
<span data-ttu-id="8e73e-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e73e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e73e-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e73e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e73e-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e73e-147">INPUTS</span></span>

## <span data-ttu-id="8e73e-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e73e-148">OUTPUTS</span></span>

### <span data-ttu-id="8e73e-149">Microsoft. Azure. Commands. insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e73e-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="8e73e-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e73e-150">NOTES</span></span>

## <span data-ttu-id="8e73e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e73e-151">RELATED LINKS</span></span>

[<span data-ttu-id="8e73e-152">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e73e-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="8e73e-153">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e73e-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


