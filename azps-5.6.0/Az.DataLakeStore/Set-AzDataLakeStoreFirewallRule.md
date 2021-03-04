---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: f344b7cfa893e7fffdb726df30918a27ce3366f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891043"
---
# <span data-ttu-id="0cd9f-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0cd9f-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="0cd9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd9f-103">Modifica a regra de firewall especificada no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="0cd9f-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0cd9f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0cd9f-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cd9f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0cd9f-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd9f-106">O cmdlet **Set-AzDataLakeStoreFirewallRule** modifica a regra de firewall especificada no Repositório de Data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="0cd9f-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0cd9f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cd9f-107">EXAMPLES</span></span>

### <span data-ttu-id="0cd9f-108">Exemplo 1: atualizar o intervalo ip inicial e final para uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="0cd9f-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="0cd9f-109">Atualiza a regra de firewall "MyFirewallRule" na conta "ContosoADL" para ter um intervalo de 127.0.0.1 - 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="0cd9f-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="0cd9f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0cd9f-110">PARAMETERS</span></span>

### <span data-ttu-id="0cd9f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0cd9f-111">-Account</span></span>
<span data-ttu-id="0cd9f-112">A conta do Data Lake Store para atualizar a regra de firewall em</span><span class="sxs-lookup"><span data-stu-id="0cd9f-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="0cd9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd9f-113">-DefaultProfile</span></span>
<span data-ttu-id="0cd9f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0cd9f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cd9f-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cd9f-115">-EndIpAddress</span></span>
<span data-ttu-id="0cd9f-116">O final do intervalo ip válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="0cd9f-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd9f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0cd9f-117">-Name</span></span>
<span data-ttu-id="0cd9f-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="0cd9f-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="0cd9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0cd9f-120">Especifica o nome do grupo de recursos que contém a conta para atualizar a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="0cd9f-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd9f-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cd9f-121">-StartIpAddress</span></span>
<span data-ttu-id="0cd9f-122">O início do intervalo ip válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="0cd9f-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="0cd9f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cd9f-123">-Confirm</span></span>
<span data-ttu-id="0cd9f-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cd9f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cd9f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cd9f-125">-WhatIf</span></span>
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

### <span data-ttu-id="0cd9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd9f-126">CommonParameters</span></span>
<span data-ttu-id="0cd9f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd9f-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd9f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd9f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cd9f-129">INPUTS</span></span>

### <span data-ttu-id="0cd9f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0cd9f-130">System.String</span></span>

## <span data-ttu-id="0cd9f-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0cd9f-131">OUTPUTS</span></span>

### <span data-ttu-id="0cd9f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0cd9f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="0cd9f-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="0cd9f-133">NOTES</span></span>

## <span data-ttu-id="0cd9f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cd9f-134">RELATED LINKS</span></span>
