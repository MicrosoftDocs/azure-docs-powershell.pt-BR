---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 3ad3e98e6fb2ab5c6e0b04495142861ecfe9e0ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431687"
---
# <span data-ttu-id="a70ad-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a70ad-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a70ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a70ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a70ad-103">Modifica a regra de firewall especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="a70ad-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a70ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a70ad-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70ad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a70ad-105">DESCRIPTION</span></span>
<span data-ttu-id="a70ad-106">O cmdlet **set-AzureRmDataLakeStoreFirewallRule** modifica a regra de firewall especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="a70ad-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a70ad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a70ad-107">EXAMPLES</span></span>

### <span data-ttu-id="a70ad-108">Exemplo 1: atualizar o intervalo de IP de início e término de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="a70ad-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="a70ad-109">Atualiza a regra de firewall "MyFirewallRule" na conta "ContosoADL" para ter um intervalo de 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="a70ad-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="a70ad-110">OS</span><span class="sxs-lookup"><span data-stu-id="a70ad-110">PARAMETERS</span></span>

### <span data-ttu-id="a70ad-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="a70ad-111">-Account</span></span>
<span data-ttu-id="a70ad-112">A conta do data Lake Store para atualizar a regra de firewall no</span><span class="sxs-lookup"><span data-stu-id="a70ad-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="a70ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70ad-113">-DefaultProfile</span></span>
<span data-ttu-id="a70ad-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a70ad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a70ad-115">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="a70ad-115">-EndIpAddress</span></span>
<span data-ttu-id="a70ad-116">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="a70ad-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70ad-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a70ad-117">-Name</span></span>
<span data-ttu-id="a70ad-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="a70ad-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="a70ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="a70ad-120">Especifica o nome do grupo de recursos que contém a conta para a qual atualizar a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="a70ad-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70ad-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a70ad-121">-StartIpAddress</span></span>
<span data-ttu-id="a70ad-122">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="a70ad-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70ad-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a70ad-123">-Confirm</span></span>
<span data-ttu-id="a70ad-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a70ad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a70ad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70ad-125">-WhatIf</span></span>
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

### <span data-ttu-id="a70ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70ad-126">CommonParameters</span></span>
<span data-ttu-id="a70ad-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a70ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70ad-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a70ad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70ad-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a70ad-129">INPUTS</span></span>

### <span data-ttu-id="a70ad-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a70ad-130">None</span></span>
<span data-ttu-id="a70ad-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a70ad-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a70ad-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a70ad-132">OUTPUTS</span></span>

### <span data-ttu-id="a70ad-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a70ad-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="a70ad-134">Os detalhes da regra de firewall atualizada.</span><span class="sxs-lookup"><span data-stu-id="a70ad-134">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="a70ad-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a70ad-135">NOTES</span></span>

## <span data-ttu-id="a70ad-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a70ad-136">RELATED LINKS</span></span>

