---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: 84da08588838982353bc8c39354452bec1a17a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432977"
---
# <span data-ttu-id="7ab53-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="7ab53-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="7ab53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ab53-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab53-103">Modifica o valor de um campo em uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="7ab53-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ab53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ab53-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ab53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ab53-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab53-106">O cmdlet **set-AzureRmAutomationConnectionFieldValue** modifica o valor de um campo em uma conexão na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab53-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="7ab53-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ab53-107">EXAMPLES</span></span>

### <span data-ttu-id="7ab53-108">Exemplo 1: alterar um valor de campo em uma conexão</span><span class="sxs-lookup"><span data-stu-id="7ab53-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="7ab53-109">Esse comando altera a ID da assinatura para a conexão do Azure chamada ContosoConnection na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="7ab53-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="7ab53-110">OS</span><span class="sxs-lookup"><span data-stu-id="7ab53-110">PARAMETERS</span></span>

### <span data-ttu-id="7ab53-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ab53-111">-AutomationAccountName</span></span>
<span data-ttu-id="7ab53-112">Especifica o nome da conta de automação para a qual esse cmdlet modifica um campo em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="7ab53-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab53-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="7ab53-113">-ConnectionFieldName</span></span>
<span data-ttu-id="7ab53-114">Especifica um nome para o campo que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7ab53-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab53-115">-DefaultProfile</span></span>
<span data-ttu-id="7ab53-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7ab53-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab53-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ab53-117">-Name</span></span>
<span data-ttu-id="7ab53-118">Especifica um nome para a conexão para a qual esse cmdlet modifica um campo.</span><span class="sxs-lookup"><span data-stu-id="7ab53-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab53-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ab53-120">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um campo em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="7ab53-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab53-121">-Valor</span><span class="sxs-lookup"><span data-stu-id="7ab53-121">-Value</span></span>
<span data-ttu-id="7ab53-122">Especifica um valor a ser modificado no campo de conexão.</span><span class="sxs-lookup"><span data-stu-id="7ab53-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab53-123">CommonParameters</span></span>
<span data-ttu-id="7ab53-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab53-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab53-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab53-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ab53-126">INPUTS</span></span>

### <span data-ttu-id="7ab53-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7ab53-127">None</span></span>
<span data-ttu-id="7ab53-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7ab53-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ab53-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ab53-129">OUTPUTS</span></span>

### <span data-ttu-id="7ab53-130">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="7ab53-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="7ab53-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ab53-131">NOTES</span></span>

## <span data-ttu-id="7ab53-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ab53-132">RELATED LINKS</span></span>

[<span data-ttu-id="7ab53-133">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7ab53-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


