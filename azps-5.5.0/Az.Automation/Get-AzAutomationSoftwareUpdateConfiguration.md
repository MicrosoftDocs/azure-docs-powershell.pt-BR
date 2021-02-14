---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115533"
---
# <span data-ttu-id="6f1be-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f1be-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6f1be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f1be-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1be-103">Obtém uma lista de configurações de atualização de software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f1be-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="6f1be-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f1be-104">SYNTAX</span></span>

### <span data-ttu-id="6f1be-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6f1be-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f1be-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f1be-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f1be-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="6f1be-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f1be-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f1be-108">DESCRIPTION</span></span>
<span data-ttu-id="6f1be-109">A Get-AzAutomationSoftwareUpdateConfiguration retorna uma lista de configurações de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="6f1be-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="6f1be-110">Para obter uma configuração de atualização de software específica, especifique o parâmetro de nome.</span><span class="sxs-lookup"><span data-stu-id="6f1be-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="6f1be-111">Você também pode listar configurações de atualização de software visando uma máquina virtual específica do Azure, especificando a ID de recurso do Azure para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6f1be-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="6f1be-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f1be-112">EXAMPLES</span></span>

### <span data-ttu-id="6f1be-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f1be-113">Example 1</span></span>
<span data-ttu-id="6f1be-114">Obter uma configuração de atualização de software de automação do azure por nome.</span><span class="sxs-lookup"><span data-stu-id="6f1be-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

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

## <span data-ttu-id="6f1be-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f1be-115">PARAMETERS</span></span>

### <span data-ttu-id="6f1be-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f1be-116">-AutomationAccountName</span></span>
<span data-ttu-id="6f1be-117">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="6f1be-117">The automation account name.</span></span>

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

### <span data-ttu-id="6f1be-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="6f1be-118">-AzureVMResourceId</span></span>
<span data-ttu-id="6f1be-119">ID de recurso do Azure da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6f1be-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="6f1be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1be-120">-DefaultProfile</span></span>
<span data-ttu-id="6f1be-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f1be-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f1be-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f1be-122">-Name</span></span>
<span data-ttu-id="6f1be-123">Nome da configuração de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="6f1be-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="6f1be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f1be-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f1be-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f1be-125">The resource group name.</span></span>

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

### <span data-ttu-id="6f1be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1be-126">CommonParameters</span></span>
<span data-ttu-id="6f1be-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f1be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1be-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f1be-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1be-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="6f1be-129">INPUTS</span></span>

### <span data-ttu-id="6f1be-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6f1be-130">System.String</span></span>

## <span data-ttu-id="6f1be-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="6f1be-131">OUTPUTS</span></span>

### <span data-ttu-id="6f1be-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f1be-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6f1be-133">Notas</span><span class="sxs-lookup"><span data-stu-id="6f1be-133">NOTES</span></span>

## <span data-ttu-id="6f1be-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f1be-134">RELATED LINKS</span></span>
