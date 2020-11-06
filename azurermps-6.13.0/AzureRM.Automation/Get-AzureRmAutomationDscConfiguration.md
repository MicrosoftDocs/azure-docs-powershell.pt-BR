---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 10e04dc24c34ba60186c8166e2626524fcc60a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426467"
---
# <span data-ttu-id="172cb-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="172cb-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="172cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="172cb-102">SYNOPSIS</span></span>
<span data-ttu-id="172cb-103">Obtém configurações DSC da automação.</span><span class="sxs-lookup"><span data-stu-id="172cb-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="172cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="172cb-104">SYNTAX</span></span>

### <span data-ttu-id="172cb-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="172cb-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="172cb-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="172cb-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="172cb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="172cb-107">DESCRIPTION</span></span>
<span data-ttu-id="172cb-108">O cmdlet **Get-AzureRmAutomationDscConfiguration** Obtém as configurações de DSC (configuração de estado desejado do APS) da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="172cb-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="172cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="172cb-109">EXAMPLES</span></span>

### <span data-ttu-id="172cb-110">Exemplo 1: obter todas as configurações de DSC</span><span class="sxs-lookup"><span data-stu-id="172cb-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="172cb-111">Esse comando obtém metadados para todas as configurações de DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="172cb-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="172cb-112">Exemplo 2: obter uma configuração DSC por nome</span><span class="sxs-lookup"><span data-stu-id="172cb-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="172cb-113">Esse comando obtém metadados para uma configuração DSC nomeada myconfiguration na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="172cb-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="172cb-114">OS</span><span class="sxs-lookup"><span data-stu-id="172cb-114">PARAMETERS</span></span>

### <span data-ttu-id="172cb-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="172cb-115">-AutomationAccountName</span></span>
<span data-ttu-id="172cb-116">Especifica o nome da conta de automação que contém as configurações de DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="172cb-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="172cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172cb-117">-DefaultProfile</span></span>
<span data-ttu-id="172cb-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="172cb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="172cb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="172cb-119">-Name</span></span>
<span data-ttu-id="172cb-120">Especifica o nome da configuração DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="172cb-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="172cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="172cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="172cb-122">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém configurações DSC.</span><span class="sxs-lookup"><span data-stu-id="172cb-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="172cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172cb-123">CommonParameters</span></span>
<span data-ttu-id="172cb-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172cb-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="172cb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172cb-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="172cb-126">INPUTS</span></span>

### <span data-ttu-id="172cb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="172cb-127">System.String</span></span>

## <span data-ttu-id="172cb-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="172cb-128">OUTPUTS</span></span>

### <span data-ttu-id="172cb-129">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="172cb-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="172cb-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="172cb-130">NOTES</span></span>

## <span data-ttu-id="172cb-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="172cb-131">RELATED LINKS</span></span>

[<span data-ttu-id="172cb-132">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="172cb-132">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="172cb-133">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="172cb-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


