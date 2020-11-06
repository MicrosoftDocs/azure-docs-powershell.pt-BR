---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 39450f979a4c79e453c66845b522aba91757f672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601072"
---
# <span data-ttu-id="b3506-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3506-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="b3506-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3506-102">SYNOPSIS</span></span>
<span data-ttu-id="b3506-103">Obtém as regras de firewall especificadas no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="b3506-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b3506-104">Se nenhuma regra de firewall for especificada, lista todas as regras de firewall da conta.</span><span class="sxs-lookup"><span data-stu-id="b3506-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="b3506-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3506-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3506-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3506-106">DESCRIPTION</span></span>
<span data-ttu-id="b3506-107">O cmdlet Get-AzDataLakeStoreFirewallRule Obtém as regras de firewall especificadas no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="b3506-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b3506-108">Se nenhuma regra de firewall for especificada, lista todas as regras de firewall da conta.</span><span class="sxs-lookup"><span data-stu-id="b3506-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="b3506-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3506-109">EXAMPLES</span></span>

### <span data-ttu-id="b3506-110">Exemplo 1: recuperar uma regra de firewall específica</span><span class="sxs-lookup"><span data-stu-id="b3506-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="b3506-111">Retorna a regra de firewall chamada "MyFirewallRule" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="b3506-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="b3506-112">Exemplo 2: listar todas as regras de firewall em uma conta</span><span class="sxs-lookup"><span data-stu-id="b3506-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="b3506-113">Retorna todas as regras de firewall na conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="b3506-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="b3506-114">OS</span><span class="sxs-lookup"><span data-stu-id="b3506-114">PARAMETERS</span></span>

### <span data-ttu-id="b3506-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="b3506-115">-Account</span></span>
<span data-ttu-id="b3506-116">A conta do data Lake Store da qual recuperar a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="b3506-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="b3506-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3506-117">-DefaultProfile</span></span>
<span data-ttu-id="b3506-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b3506-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3506-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3506-119">-Name</span></span>
<span data-ttu-id="b3506-120">O nome da regra de firewall a ser recuperada</span><span class="sxs-lookup"><span data-stu-id="b3506-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="b3506-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3506-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3506-122">Nome do grupo de recursos sob o qual deseja recuperar a regra de firewall especificada da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="b3506-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="b3506-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3506-123">CommonParameters</span></span>
<span data-ttu-id="b3506-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3506-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3506-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3506-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3506-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3506-126">INPUTS</span></span>

### <span data-ttu-id="b3506-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b3506-127">System.String</span></span>

## <span data-ttu-id="b3506-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3506-128">OUTPUTS</span></span>

### <span data-ttu-id="b3506-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3506-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="b3506-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3506-130">NOTES</span></span>

## <span data-ttu-id="b3506-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3506-131">RELATED LINKS</span></span>
