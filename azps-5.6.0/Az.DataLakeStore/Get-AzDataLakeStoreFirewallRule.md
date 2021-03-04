---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 580b5518e1fc0894a51920e781464258bef9e9cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887219"
---
# <span data-ttu-id="f1da6-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f1da6-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f1da6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1da6-102">SYNOPSIS</span></span>
<span data-ttu-id="f1da6-103">Obtém as regras de firewall especificadas no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="f1da6-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f1da6-104">Se nenhuma regra de firewall for especificada, lista todas as regras de firewall para a conta.</span><span class="sxs-lookup"><span data-stu-id="f1da6-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="f1da6-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f1da6-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1da6-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f1da6-106">DESCRIPTION</span></span>
<span data-ttu-id="f1da6-107">O Get-AzDataLakeStoreFirewallRule cmdlet obtém as regras de firewall especificadas no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="f1da6-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f1da6-108">Se nenhuma regra de firewall for especificada, lista todas as regras de firewall para a conta.</span><span class="sxs-lookup"><span data-stu-id="f1da6-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="f1da6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1da6-109">EXAMPLES</span></span>

### <span data-ttu-id="f1da6-110">Exemplo 1: Recuperar uma regra de firewall específica</span><span class="sxs-lookup"><span data-stu-id="f1da6-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="f1da6-111">Retorna a regra de firewall chamada "MyFirewallRule" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="f1da6-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="f1da6-112">Exemplo 2: Listar todas as regras de firewall em uma conta</span><span class="sxs-lookup"><span data-stu-id="f1da6-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="f1da6-113">Retorna todas as regras de firewall na conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="f1da6-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="f1da6-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f1da6-114">PARAMETERS</span></span>

### <span data-ttu-id="f1da6-115">-Account</span><span class="sxs-lookup"><span data-stu-id="f1da6-115">-Account</span></span>
<span data-ttu-id="f1da6-116">A conta do Data Lake Store para recuperar a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="f1da6-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="f1da6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1da6-117">-DefaultProfile</span></span>
<span data-ttu-id="f1da6-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f1da6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1da6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f1da6-119">-Name</span></span>
<span data-ttu-id="f1da6-120">O nome da regra de firewall a ser recuperada</span><span class="sxs-lookup"><span data-stu-id="f1da6-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="f1da6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1da6-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1da6-122">Nome do grupo de recursos no qual deseja recuperar a regra de firewall especificada da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="f1da6-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1da6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1da6-123">CommonParameters</span></span>
<span data-ttu-id="f1da6-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1da6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1da6-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1da6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1da6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1da6-126">INPUTS</span></span>

### <span data-ttu-id="f1da6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f1da6-127">System.String</span></span>

## <span data-ttu-id="f1da6-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f1da6-128">OUTPUTS</span></span>

### <span data-ttu-id="f1da6-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f1da6-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f1da6-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="f1da6-130">NOTES</span></span>

## <span data-ttu-id="f1da6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1da6-131">RELATED LINKS</span></span>
