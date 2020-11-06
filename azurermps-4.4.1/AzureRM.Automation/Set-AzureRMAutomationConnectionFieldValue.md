---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: c3f889f45a90b127287821afb789eab2908faffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440222"
---
# <span data-ttu-id="8eb26-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="8eb26-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="8eb26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eb26-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb26-103">Modifica o valor de um campo em uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="8eb26-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eb26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8eb26-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8eb26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8eb26-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb26-106">O cmdlet **set-AzureRmAutomationConnectionFieldValue** modifica o valor de um campo em uma conexão na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="8eb26-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="8eb26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8eb26-107">EXAMPLES</span></span>

### <span data-ttu-id="8eb26-108">Exemplo 1: alterar um valor de campo em uma conexão</span><span class="sxs-lookup"><span data-stu-id="8eb26-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="8eb26-109">Esse comando altera a ID da assinatura para a conexão do Azure chamada ContosoConnection na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="8eb26-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="8eb26-110">OS</span><span class="sxs-lookup"><span data-stu-id="8eb26-110">PARAMETERS</span></span>

### <span data-ttu-id="8eb26-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8eb26-111">-AutomationAccountName</span></span>
<span data-ttu-id="8eb26-112">Especifica o nome da conta de automação para a qual esse cmdlet modifica um campo em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="8eb26-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb26-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="8eb26-113">-ConnectionFieldName</span></span>
<span data-ttu-id="8eb26-114">Especifica um nome para o campo que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8eb26-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8eb26-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8eb26-115">-Name</span></span>
<span data-ttu-id="8eb26-116">Especifica um nome para a conexão para a qual esse cmdlet modifica um campo.</span><span class="sxs-lookup"><span data-stu-id="8eb26-116">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb26-117">-ResourceGroupName</span></span>
<span data-ttu-id="8eb26-118">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um campo em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="8eb26-118">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb26-119">-Valor</span><span class="sxs-lookup"><span data-stu-id="8eb26-119">-Value</span></span>
<span data-ttu-id="8eb26-120">Especifica um valor a ser modificado no campo de conexão.</span><span class="sxs-lookup"><span data-stu-id="8eb26-120">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb26-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb26-121">-DefaultProfile</span></span>
<span data-ttu-id="8eb26-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8eb26-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8eb26-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb26-123">CommonParameters</span></span>
<span data-ttu-id="8eb26-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb26-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb26-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb26-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb26-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8eb26-126">INPUTS</span></span>

## <span data-ttu-id="8eb26-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8eb26-127">OUTPUTS</span></span>

### <span data-ttu-id="8eb26-128">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="8eb26-128">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="8eb26-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8eb26-129">NOTES</span></span>

## <span data-ttu-id="8eb26-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eb26-130">RELATED LINKS</span></span>

[<span data-ttu-id="8eb26-131">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="8eb26-131">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

