---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: c1e4c3f748df4808fe570e95150450d3b3987d00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440473"
---
# <span data-ttu-id="58c99-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="58c99-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="58c99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58c99-102">SYNOPSIS</span></span>
<span data-ttu-id="58c99-103">Adiciona uma regra de firewall à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="58c99-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58c99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c99-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c99-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58c99-105">DESCRIPTION</span></span>
<span data-ttu-id="58c99-106">O cmdlet **Add-AzureRmDataLakeStoreFirewallRule** adiciona uma regra de firewall à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="58c99-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="58c99-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58c99-107">EXAMPLES</span></span>

### <span data-ttu-id="58c99-108">Exemplo 1: adicionar uma nova regra de firewall a uma conta do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="58c99-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="58c99-109">Isso cria uma nova regra de firewall chamada "myrule" na conta "ContosoADL" com um intervalo IP de 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="58c99-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="58c99-110">OS</span><span class="sxs-lookup"><span data-stu-id="58c99-110">PARAMETERS</span></span>

### <span data-ttu-id="58c99-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="58c99-111">-Account</span></span>
<span data-ttu-id="58c99-112">A conta do data Lake Store para a qual adicionar a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="58c99-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c99-113">-DefaultProfile</span></span>
<span data-ttu-id="58c99-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="58c99-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c99-115">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="58c99-115">-EndIpAddress</span></span>
<span data-ttu-id="58c99-116">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="58c99-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c99-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="58c99-117">-Name</span></span>
<span data-ttu-id="58c99-118">O nome da regra de firewall a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="58c99-118">The name of the firewall rule to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c99-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c99-119">-ResourceGroupName</span></span>
<span data-ttu-id="58c99-120">Nome do grupo de recursos sob o qual a conta para adicionar a regra de firewall é.</span><span class="sxs-lookup"><span data-stu-id="58c99-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c99-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="58c99-121">-StartIpAddress</span></span>
<span data-ttu-id="58c99-122">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="58c99-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c99-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58c99-123">-Confirm</span></span>
<span data-ttu-id="58c99-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58c99-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c99-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c99-125">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c99-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c99-126">CommonParameters</span></span>
<span data-ttu-id="58c99-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c99-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c99-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c99-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c99-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58c99-129">INPUTS</span></span>

### <span data-ttu-id="58c99-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="58c99-130">None</span></span>
<span data-ttu-id="58c99-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="58c99-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58c99-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58c99-132">OUTPUTS</span></span>

### <span data-ttu-id="58c99-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="58c99-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="58c99-134">A regra de firewall que foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="58c99-134">The firewall rule that was added.</span></span>

## <span data-ttu-id="58c99-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58c99-135">NOTES</span></span>

## <span data-ttu-id="58c99-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58c99-136">RELATED LINKS</span></span>

