---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f4d17fa6cdcb64aab2ab373420891f686facfdf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433330"
---
# <span data-ttu-id="dd6f9-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd6f9-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="dd6f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6f9-103">Obtém uma lista de configurações de atualização de software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-103">Gets a list of azure automation software update configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd6f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd6f9-104">SYNTAX</span></span>

### <span data-ttu-id="dd6f9-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd6f9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd6f9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dd6f9-106">ByName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd6f9-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="dd6f9-107">ByVMId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd6f9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd6f9-108">DESCRIPTION</span></span>
<span data-ttu-id="dd6f9-109">A Get-AzureRmAutomationSoftwareUpdateConfiguration retorna uma lista de configurações de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-109">The Get-AzureRmAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="dd6f9-110">Para obter uma configuração de atualização de software específica, especifique o parâmetro Name.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="dd6f9-111">Você também pode listar configurações de atualização de software direcionando a máquina virtual do Azure específica especificando a ID de recurso do Azure para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="dd6f9-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd6f9-112">EXAMPLES</span></span>

### <span data-ttu-id="dd6f9-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd6f9-113">Example 1</span></span>
<span data-ttu-id="dd6f9-114">Obtenha uma configuração de atualização do software de automação do Azure por nome.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="dd6f9-115">OS</span><span class="sxs-lookup"><span data-stu-id="dd6f9-115">PARAMETERS</span></span>

### <span data-ttu-id="dd6f9-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd6f9-116">-AutomationAccountName</span></span>
<span data-ttu-id="dd6f9-117">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-117">The automation account name.</span></span>

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

### <span data-ttu-id="dd6f9-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="dd6f9-118">-AzureVMResourceId</span></span>
<span data-ttu-id="dd6f9-119">ID de recurso do Azure da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6f9-120">-DefaultProfile</span></span>
<span data-ttu-id="dd6f9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd6f9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd6f9-122">-Name</span></span>
<span data-ttu-id="dd6f9-123">Nome da configuração de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd6f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd6f9-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-125">The resource group name.</span></span>

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

### <span data-ttu-id="dd6f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6f9-126">CommonParameters</span></span>
<span data-ttu-id="dd6f9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd6f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6f9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd6f9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6f9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd6f9-129">INPUTS</span></span>

### <span data-ttu-id="dd6f9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dd6f9-130">System.String</span></span>

## <span data-ttu-id="dd6f9-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd6f9-131">OUTPUTS</span></span>

### <span data-ttu-id="dd6f9-132">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd6f9-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="dd6f9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd6f9-133">NOTES</span></span>

## <span data-ttu-id="dd6f9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd6f9-134">RELATED LINKS</span></span>
