---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 9fa890ee6102f4751b62325b3cc3669d337cb6c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596875"
---
# <span data-ttu-id="67dc7-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67dc7-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="67dc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="67dc7-103">Adiciona uma regra de firewall à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="67dc7-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="67dc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67dc7-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67dc7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="67dc7-106">O cmdlet **Add-AzDataLakeStoreFirewallRule** adiciona uma regra de firewall à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="67dc7-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="67dc7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67dc7-107">EXAMPLES</span></span>

### <span data-ttu-id="67dc7-108">Exemplo 1: adicionar uma nova regra de firewall a uma conta do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="67dc7-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="67dc7-109">Isso cria uma nova regra de firewall chamada "myrule" na conta "ContosoADL" com um intervalo IP de 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="67dc7-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="67dc7-110">OS</span><span class="sxs-lookup"><span data-stu-id="67dc7-110">PARAMETERS</span></span>

### <span data-ttu-id="67dc7-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="67dc7-111">-Account</span></span>
<span data-ttu-id="67dc7-112">A conta do data Lake Store para a qual adicionar a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="67dc7-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="67dc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67dc7-113">-DefaultProfile</span></span>
<span data-ttu-id="67dc7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="67dc7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67dc7-115">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="67dc7-115">-EndIpAddress</span></span>
<span data-ttu-id="67dc7-116">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="67dc7-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="67dc7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="67dc7-117">-Name</span></span>
<span data-ttu-id="67dc7-118">O nome da regra de firewall a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="67dc7-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="67dc7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67dc7-119">-ResourceGroupName</span></span>
<span data-ttu-id="67dc7-120">Nome do grupo de recursos sob o qual a conta para adicionar a regra de firewall é.</span><span class="sxs-lookup"><span data-stu-id="67dc7-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="67dc7-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="67dc7-121">-StartIpAddress</span></span>
<span data-ttu-id="67dc7-122">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="67dc7-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="67dc7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67dc7-123">-Confirm</span></span>
<span data-ttu-id="67dc7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67dc7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67dc7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67dc7-125">-WhatIf</span></span>
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

### <span data-ttu-id="67dc7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67dc7-126">CommonParameters</span></span>
<span data-ttu-id="67dc7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67dc7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67dc7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67dc7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67dc7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67dc7-129">INPUTS</span></span>

### <span data-ttu-id="67dc7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="67dc7-130">System.String</span></span>

## <span data-ttu-id="67dc7-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67dc7-131">OUTPUTS</span></span>

### <span data-ttu-id="67dc7-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67dc7-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="67dc7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67dc7-133">NOTES</span></span>

## <span data-ttu-id="67dc7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67dc7-134">RELATED LINKS</span></span>
