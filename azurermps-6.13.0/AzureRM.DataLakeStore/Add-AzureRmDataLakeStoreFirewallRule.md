---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: d990f36fc68878a1751ad41ccfde51e4bbd82d2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431991"
---
# <span data-ttu-id="cdba6-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cdba6-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="cdba6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdba6-102">SYNOPSIS</span></span>
<span data-ttu-id="cdba6-103">Adiciona uma regra de firewall à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cdba6-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdba6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdba6-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdba6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdba6-105">DESCRIPTION</span></span>
<span data-ttu-id="cdba6-106">O cmdlet **Add-AzureRmDataLakeStoreFirewallRule** adiciona uma regra de firewall à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cdba6-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="cdba6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdba6-107">EXAMPLES</span></span>

### <span data-ttu-id="cdba6-108">Exemplo 1: adicionar uma nova regra de firewall a uma conta do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="cdba6-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="cdba6-109">Isso cria uma nova regra de firewall chamada "myrule" na conta "ContosoADL" com um intervalo IP de 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="cdba6-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="cdba6-110">OS</span><span class="sxs-lookup"><span data-stu-id="cdba6-110">PARAMETERS</span></span>

### <span data-ttu-id="cdba6-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="cdba6-111">-Account</span></span>
<span data-ttu-id="cdba6-112">A conta do data Lake Store para a qual adicionar a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="cdba6-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="cdba6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdba6-113">-DefaultProfile</span></span>
<span data-ttu-id="cdba6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cdba6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdba6-115">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="cdba6-115">-EndIpAddress</span></span>
<span data-ttu-id="cdba6-116">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="cdba6-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdba6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdba6-117">-Name</span></span>
<span data-ttu-id="cdba6-118">O nome da regra de firewall a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="cdba6-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="cdba6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdba6-119">-ResourceGroupName</span></span>
<span data-ttu-id="cdba6-120">Nome do grupo de recursos sob o qual a conta para adicionar a regra de firewall é.</span><span class="sxs-lookup"><span data-stu-id="cdba6-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="cdba6-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="cdba6-121">-StartIpAddress</span></span>
<span data-ttu-id="cdba6-122">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="cdba6-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdba6-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cdba6-123">-Confirm</span></span>
<span data-ttu-id="cdba6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdba6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdba6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdba6-125">-WhatIf</span></span>
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

### <span data-ttu-id="cdba6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdba6-126">CommonParameters</span></span>
<span data-ttu-id="cdba6-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdba6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdba6-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdba6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdba6-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdba6-129">INPUTS</span></span>

### <span data-ttu-id="cdba6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cdba6-130">System.String</span></span>

## <span data-ttu-id="cdba6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdba6-131">OUTPUTS</span></span>

### <span data-ttu-id="cdba6-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cdba6-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="cdba6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdba6-133">NOTES</span></span>

## <span data-ttu-id="cdba6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdba6-134">RELATED LINKS</span></span>
