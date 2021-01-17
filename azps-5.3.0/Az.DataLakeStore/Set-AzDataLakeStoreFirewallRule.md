---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426601"
---
# <span data-ttu-id="3615a-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3615a-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="3615a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3615a-102">SYNOPSIS</span></span>
<span data-ttu-id="3615a-103">Modifica a regra de firewall especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="3615a-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3615a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3615a-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3615a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3615a-105">DESCRIPTION</span></span>
<span data-ttu-id="3615a-106">O cmdlet **set-AzDataLakeStoreFirewallRule** modifica a regra de firewall especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="3615a-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3615a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3615a-107">EXAMPLES</span></span>

### <span data-ttu-id="3615a-108">Exemplo 1: atualizar o intervalo de IP de início e término de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="3615a-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="3615a-109">Atualiza a regra de firewall "MyFirewallRule" na conta "ContosoADL" para ter um intervalo de 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="3615a-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="3615a-110">OS</span><span class="sxs-lookup"><span data-stu-id="3615a-110">PARAMETERS</span></span>

### <span data-ttu-id="3615a-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="3615a-111">-Account</span></span>
<span data-ttu-id="3615a-112">A conta do data Lake Store para atualizar a regra de firewall no</span><span class="sxs-lookup"><span data-stu-id="3615a-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="3615a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3615a-113">-DefaultProfile</span></span>
<span data-ttu-id="3615a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3615a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3615a-115">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="3615a-115">-EndIpAddress</span></span>
<span data-ttu-id="3615a-116">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="3615a-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="3615a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3615a-117">-Name</span></span>
<span data-ttu-id="3615a-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="3615a-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="3615a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3615a-119">-ResourceGroupName</span></span>
<span data-ttu-id="3615a-120">Especifica o nome do grupo de recursos que contém a conta para a qual atualizar a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="3615a-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="3615a-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3615a-121">-StartIpAddress</span></span>
<span data-ttu-id="3615a-122">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="3615a-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="3615a-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3615a-123">-Confirm</span></span>
<span data-ttu-id="3615a-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3615a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3615a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3615a-125">-WhatIf</span></span>
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

### <span data-ttu-id="3615a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3615a-126">CommonParameters</span></span>
<span data-ttu-id="3615a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3615a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3615a-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3615a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3615a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3615a-129">INPUTS</span></span>

### <span data-ttu-id="3615a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3615a-130">System.String</span></span>

## <span data-ttu-id="3615a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3615a-131">OUTPUTS</span></span>

### <span data-ttu-id="3615a-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3615a-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="3615a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3615a-133">NOTES</span></span>

## <span data-ttu-id="3615a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3615a-134">RELATED LINKS</span></span>
