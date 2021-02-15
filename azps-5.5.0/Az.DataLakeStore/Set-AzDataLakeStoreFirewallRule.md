---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111942"
---
# <span data-ttu-id="5accd-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5accd-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="5accd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5accd-102">SYNOPSIS</span></span>
<span data-ttu-id="5accd-103">Modifica a regra de firewall especificada no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="5accd-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5accd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5accd-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5accd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5accd-105">DESCRIPTION</span></span>
<span data-ttu-id="5accd-106">O cmdlet **Set-AzDataLakeStoreFirewallRule** modifica a regra de firewall especificada no Repositório de Dados especificado.</span><span class="sxs-lookup"><span data-stu-id="5accd-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5accd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5accd-107">EXAMPLES</span></span>

### <span data-ttu-id="5accd-108">Exemplo 1: Atualizar o intervalo IP inicial e final para uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="5accd-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="5accd-109">Atualiza a regra de firewall "MyFirewallRule" na conta "ContosoADL" para ter um intervalo de 127.0.0.1 - 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="5accd-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="5accd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5accd-110">PARAMETERS</span></span>

### <span data-ttu-id="5accd-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="5accd-111">-Account</span></span>
<span data-ttu-id="5accd-112">A conta do Data Lake Store para atualizar a regra de firewall em</span><span class="sxs-lookup"><span data-stu-id="5accd-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="5accd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5accd-113">-DefaultProfile</span></span>
<span data-ttu-id="5accd-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5accd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5accd-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5accd-115">-EndIpAddress</span></span>
<span data-ttu-id="5accd-116">O fim do intervalo ip válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="5accd-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="5accd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5accd-117">-Name</span></span>
<span data-ttu-id="5accd-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="5accd-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="5accd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5accd-119">-ResourceGroupName</span></span>
<span data-ttu-id="5accd-120">Especifica o nome do grupo de recursos que contém a conta para atualizar a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="5accd-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="5accd-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5accd-121">-StartIpAddress</span></span>
<span data-ttu-id="5accd-122">O início do intervalo ip válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="5accd-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="5accd-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5accd-123">-Confirm</span></span>
<span data-ttu-id="5accd-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5accd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5accd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5accd-125">-WhatIf</span></span>
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

### <span data-ttu-id="5accd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5accd-126">CommonParameters</span></span>
<span data-ttu-id="5accd-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5accd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5accd-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5accd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5accd-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="5accd-129">INPUTS</span></span>

### <span data-ttu-id="5accd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5accd-130">System.String</span></span>

## <span data-ttu-id="5accd-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="5accd-131">OUTPUTS</span></span>

### <span data-ttu-id="5accd-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5accd-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="5accd-133">Notas</span><span class="sxs-lookup"><span data-stu-id="5accd-133">NOTES</span></span>

## <span data-ttu-id="5accd-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5accd-134">RELATED LINKS</span></span>
