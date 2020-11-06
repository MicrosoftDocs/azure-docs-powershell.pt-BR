---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 9d0b360e7284086b1cfadcba6ad17c47c22b6cb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427558"
---
# <span data-ttu-id="51076-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51076-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="51076-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51076-102">SYNOPSIS</span></span>
<span data-ttu-id="51076-103">Remove a regra de firewall especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="51076-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51076-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51076-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51076-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51076-105">DESCRIPTION</span></span>
<span data-ttu-id="51076-106">O cmdlet **Remove-AzureRmDataLakeStoreFirewallRule** remove a regra de firewall especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="51076-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="51076-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51076-107">EXAMPLES</span></span>

### <span data-ttu-id="51076-108">Exemplo 1: remover uma regra de firewall de uma conta</span><span class="sxs-lookup"><span data-stu-id="51076-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="51076-109">Remove a regra de firewall "MyFirewallRule" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="51076-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="51076-110">OS</span><span class="sxs-lookup"><span data-stu-id="51076-110">PARAMETERS</span></span>

### <span data-ttu-id="51076-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="51076-111">-Account</span></span>
<span data-ttu-id="51076-112">A conta do data Lake Store para atualizar a regra de firewall no</span><span class="sxs-lookup"><span data-stu-id="51076-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="51076-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51076-113">-DefaultProfile</span></span>
<span data-ttu-id="51076-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="51076-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51076-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="51076-115">-Name</span></span>
<span data-ttu-id="51076-116">O nome da regra de firewall a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="51076-116">The name of the firewall rule to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51076-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51076-117">-PassThru</span></span>
<span data-ttu-id="51076-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="51076-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51076-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51076-119">-ResourceGroupName</span></span>
<span data-ttu-id="51076-120">Especifica o nome do grupo de recursos que contém a conta a partir da qual a regra de firewall será removida.</span><span class="sxs-lookup"><span data-stu-id="51076-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="51076-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51076-121">-Confirm</span></span>
<span data-ttu-id="51076-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51076-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51076-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51076-123">-WhatIf</span></span>
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

### <span data-ttu-id="51076-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51076-124">CommonParameters</span></span>
<span data-ttu-id="51076-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51076-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51076-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51076-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51076-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51076-127">INPUTS</span></span>

### <span data-ttu-id="51076-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="51076-128">None</span></span>
<span data-ttu-id="51076-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="51076-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51076-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51076-130">OUTPUTS</span></span>

### <span data-ttu-id="51076-131">bool</span><span class="sxs-lookup"><span data-stu-id="51076-131">bool</span></span>
<span data-ttu-id="51076-132">Se PassThru for especificado, retornará true após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="51076-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="51076-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51076-133">NOTES</span></span>

## <span data-ttu-id="51076-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51076-134">RELATED LINKS</span></span>

