---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 7a753f721e008a0c40f6a690d5c595a524ddc12b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886981"
---
# <span data-ttu-id="34b75-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="34b75-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="34b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34b75-102">SYNOPSIS</span></span>
<span data-ttu-id="34b75-103">Remove a regra de firewall especificada no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="34b75-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="34b75-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="34b75-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34b75-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="34b75-105">DESCRIPTION</span></span>
<span data-ttu-id="34b75-106">O cmdlet **Remove-AzDataLakeStoreFirewallRule** remove a regra de firewall especificada no Repositório de Data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="34b75-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="34b75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34b75-107">EXAMPLES</span></span>

### <span data-ttu-id="34b75-108">Exemplo 1: Remover uma regra de firewall de uma conta</span><span class="sxs-lookup"><span data-stu-id="34b75-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="34b75-109">Remove a regra de firewall "MyFirewallRule" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="34b75-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="34b75-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="34b75-110">PARAMETERS</span></span>

### <span data-ttu-id="34b75-111">-Account</span><span class="sxs-lookup"><span data-stu-id="34b75-111">-Account</span></span>
<span data-ttu-id="34b75-112">A conta do Data Lake Store para atualizar a regra de firewall em</span><span class="sxs-lookup"><span data-stu-id="34b75-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b75-113">-DefaultProfile</span></span>
<span data-ttu-id="34b75-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="34b75-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34b75-115">-Name</span><span class="sxs-lookup"><span data-stu-id="34b75-115">-Name</span></span>
<span data-ttu-id="34b75-116">O nome da regra de firewall a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="34b75-116">The name of the firewall rule to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b75-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34b75-117">-PassThru</span></span>
<span data-ttu-id="34b75-118">Indica que uma resposta booleana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="34b75-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b75-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b75-119">-ResourceGroupName</span></span>
<span data-ttu-id="34b75-120">Especifica o nome do grupo de recursos que contém a conta para remover a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="34b75-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b75-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34b75-121">-Confirm</span></span>
<span data-ttu-id="34b75-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34b75-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34b75-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b75-123">-WhatIf</span></span>
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

### <span data-ttu-id="34b75-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b75-124">CommonParameters</span></span>
<span data-ttu-id="34b75-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b75-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b75-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b75-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b75-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34b75-127">INPUTS</span></span>

### <span data-ttu-id="34b75-128">System.String</span><span class="sxs-lookup"><span data-stu-id="34b75-128">System.String</span></span>

### <span data-ttu-id="34b75-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="34b75-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="34b75-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="34b75-130">OUTPUTS</span></span>

### <span data-ttu-id="34b75-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34b75-131">System.Boolean</span></span>

## <span data-ttu-id="34b75-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="34b75-132">NOTES</span></span>

## <span data-ttu-id="34b75-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34b75-133">RELATED LINKS</span></span>
