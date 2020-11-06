---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: eaa1195e5cb853111b6e75efbff7e37bc8ff6881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426448"
---
# <span data-ttu-id="8a00b-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8a00b-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="8a00b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a00b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a00b-103">Modifica a configuração do nó para a qual um nó DSC está mapeado.</span><span class="sxs-lookup"><span data-stu-id="8a00b-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a00b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a00b-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a00b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a00b-105">DESCRIPTION</span></span>
<span data-ttu-id="8a00b-106">O cmdlet **set-AzureRmAutomationDscNode** modifica uma configuração de nó DSC (configuração de estado desejado APS).</span><span class="sxs-lookup"><span data-stu-id="8a00b-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="8a00b-107">A automação do Azure armazena a configuração do nó DSC como um documento de configuração do MOF (formato de objeto gerenciado).</span><span class="sxs-lookup"><span data-stu-id="8a00b-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="8a00b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a00b-108">EXAMPLES</span></span>

### <span data-ttu-id="8a00b-109">Exemplo 1: modificar o mapeamento de configuração do nó</span><span class="sxs-lookup"><span data-stu-id="8a00b-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="8a00b-110">Esse comando atribui a configuração de nó chamada contoso. NodeConfiguration01 ao nó que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="8a00b-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="8a00b-111">OS</span><span class="sxs-lookup"><span data-stu-id="8a00b-111">PARAMETERS</span></span>

### <span data-ttu-id="8a00b-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8a00b-112">-AutomationAccountName</span></span>
<span data-ttu-id="8a00b-113">Especifica o nome da conta de automação que contém o nó DSC para o qual esse cmdlet modifica a configuração.</span><span class="sxs-lookup"><span data-stu-id="8a00b-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="8a00b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a00b-114">-DefaultProfile</span></span>
<span data-ttu-id="8a00b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8a00b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a00b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8a00b-116">-Force</span></span>
<span data-ttu-id="8a00b-117">ps_force o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8a00b-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a00b-118">-ID</span><span class="sxs-lookup"><span data-stu-id="8a00b-118">-Id</span></span>
<span data-ttu-id="8a00b-119">Especifica a ID exclusiva do nó DSC para o qual esse cmdlet modifica a configuração.</span><span class="sxs-lookup"><span data-stu-id="8a00b-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8a00b-120">-NodeConfigurationName</span></span>
<span data-ttu-id="8a00b-121">Especifica o nome da configuração de nó para a qual esse cmdlet mapeia o nó.</span><span class="sxs-lookup"><span data-stu-id="8a00b-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="8a00b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a00b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a00b-123">Especifica o nome de um grupo de recursos em que esse cmdlet modifica uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="8a00b-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="8a00b-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8a00b-124">-Confirm</span></span>
<span data-ttu-id="8a00b-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a00b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a00b-126">-WhatIf</span></span>
<span data-ttu-id="8a00b-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8a00b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a00b-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a00b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a00b-129">CommonParameters</span></span>
<span data-ttu-id="8a00b-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a00b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a00b-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a00b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a00b-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a00b-132">INPUTS</span></span>

### <span data-ttu-id="8a00b-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8a00b-133">System.Guid</span></span>

### <span data-ttu-id="8a00b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8a00b-134">System.String</span></span>

## <span data-ttu-id="8a00b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a00b-135">OUTPUTS</span></span>

### <span data-ttu-id="8a00b-136">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="8a00b-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="8a00b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a00b-137">NOTES</span></span>

## <span data-ttu-id="8a00b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a00b-138">RELATED LINKS</span></span>

[<span data-ttu-id="8a00b-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8a00b-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="8a00b-140">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8a00b-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="8a00b-141">Cancelar registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8a00b-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


