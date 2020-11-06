---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: e0e74aa910c11a10c26cf6bed623d2e2c02f93ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428615"
---
# <span data-ttu-id="41d60-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d60-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="41d60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41d60-102">SYNOPSIS</span></span>
<span data-ttu-id="41d60-103">Remove uma configuração de atualização do software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="41d60-103">Removes an azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41d60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41d60-104">SYNTAX</span></span>

### <span data-ttu-id="41d60-105">BySucName (padrão)</span><span class="sxs-lookup"><span data-stu-id="41d60-105">BySucName (Default)</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41d60-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="41d60-106">BySuc</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d60-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41d60-107">DESCRIPTION</span></span>
<span data-ttu-id="41d60-108">Este cmdlet removeu uma configuração de atualização do software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="41d60-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="41d60-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41d60-109">EXAMPLES</span></span>

### <span data-ttu-id="41d60-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41d60-110">Example 1</span></span>
<span data-ttu-id="41d60-111">Este exemplo mostra como remover "MyUpdateConfiguration" da conta de automação</span><span class="sxs-lookup"><span data-stu-id="41d60-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="41d60-112">OS</span><span class="sxs-lookup"><span data-stu-id="41d60-112">PARAMETERS</span></span>

### <span data-ttu-id="41d60-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="41d60-113">-AutomationAccountName</span></span>
<span data-ttu-id="41d60-114">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="41d60-114">The automation account name.</span></span>

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

### <span data-ttu-id="41d60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d60-115">-DefaultProfile</span></span>
<span data-ttu-id="41d60-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41d60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d60-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="41d60-117">-Name</span></span>
<span data-ttu-id="41d60-118">Nome da configuração de atualização de software a ser removida.</span><span class="sxs-lookup"><span data-stu-id="41d60-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d60-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41d60-119">-PassThru</span></span>
<span data-ttu-id="41d60-120">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="41d60-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="41d60-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="41d60-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41d60-122">-ResourceGroupName</span></span>
<span data-ttu-id="41d60-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41d60-123">The resource group name.</span></span>

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

### <span data-ttu-id="41d60-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d60-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="41d60-125">A configuração de atualização de software a ser removida.</span><span class="sxs-lookup"><span data-stu-id="41d60-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d60-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41d60-126">-Confirm</span></span>
<span data-ttu-id="41d60-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d60-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d60-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d60-128">-WhatIf</span></span>
<span data-ttu-id="41d60-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41d60-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41d60-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41d60-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d60-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d60-131">CommonParameters</span></span>
<span data-ttu-id="41d60-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d60-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d60-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d60-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d60-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41d60-134">INPUTS</span></span>

### <span data-ttu-id="41d60-135">System. String</span><span class="sxs-lookup"><span data-stu-id="41d60-135">System.String</span></span>

### <span data-ttu-id="41d60-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d60-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="41d60-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41d60-137">OUTPUTS</span></span>

### <span data-ttu-id="41d60-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="41d60-138">System.Object</span></span>
## <span data-ttu-id="41d60-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41d60-139">NOTES</span></span>

## <span data-ttu-id="41d60-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41d60-140">RELATED LINKS</span></span>
