---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111760"
---
# <span data-ttu-id="bb12a-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb12a-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="bb12a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb12a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb12a-103">Remove a regra de firewall especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="bb12a-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="bb12a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb12a-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb12a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb12a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb12a-106">O cmdlet **Remove-AzDataLakeStoreFirewallRule** remove a regra de firewall especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="bb12a-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="bb12a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb12a-107">EXAMPLES</span></span>

### <span data-ttu-id="bb12a-108">Exemplo 1: remover uma regra de firewall de uma conta</span><span class="sxs-lookup"><span data-stu-id="bb12a-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="bb12a-109">Remove a regra de firewall "MyFirewallRule" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="bb12a-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="bb12a-110">OS</span><span class="sxs-lookup"><span data-stu-id="bb12a-110">PARAMETERS</span></span>

### <span data-ttu-id="bb12a-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="bb12a-111">-Account</span></span>
<span data-ttu-id="bb12a-112">A conta do data Lake Store para atualizar a regra de firewall no</span><span class="sxs-lookup"><span data-stu-id="bb12a-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="bb12a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb12a-113">-DefaultProfile</span></span>
<span data-ttu-id="bb12a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bb12a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb12a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb12a-115">-Name</span></span>
<span data-ttu-id="bb12a-116">O nome da regra de firewall a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="bb12a-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="bb12a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb12a-117">-PassThru</span></span>
<span data-ttu-id="bb12a-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="bb12a-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="bb12a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb12a-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb12a-120">Especifica o nome do grupo de recursos que contém a conta a partir da qual a regra de firewall será removida.</span><span class="sxs-lookup"><span data-stu-id="bb12a-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="bb12a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb12a-121">-Confirm</span></span>
<span data-ttu-id="bb12a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb12a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb12a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb12a-123">-WhatIf</span></span>
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

### <span data-ttu-id="bb12a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb12a-124">CommonParameters</span></span>
<span data-ttu-id="bb12a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb12a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb12a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb12a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb12a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb12a-127">INPUTS</span></span>

### <span data-ttu-id="bb12a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bb12a-128">System.String</span></span>

### <span data-ttu-id="bb12a-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb12a-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bb12a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb12a-130">OUTPUTS</span></span>

### <span data-ttu-id="bb12a-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb12a-131">System.Boolean</span></span>

## <span data-ttu-id="bb12a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb12a-132">NOTES</span></span>

## <span data-ttu-id="bb12a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb12a-133">RELATED LINKS</span></span>
