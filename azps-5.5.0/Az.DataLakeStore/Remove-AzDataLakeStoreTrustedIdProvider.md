---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127029"
---
# <span data-ttu-id="2dda4-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="2dda4-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="2dda4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dda4-102">SYNOPSIS</span></span>
<span data-ttu-id="2dda4-103">Remove o provedor de identidade confiável especificado no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="2dda4-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="2dda4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dda4-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dda4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2dda4-105">DESCRIPTION</span></span>
<span data-ttu-id="2dda4-106">O cmdlet **Remove-AzDataLakeStoreTrustedIdProvider** remove o provedor de identidade confiável especificado na Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="2dda4-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="2dda4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2dda4-107">EXAMPLES</span></span>

### <span data-ttu-id="2dda4-108">Exemplo 1: Remover um provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="2dda4-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="2dda4-109">Remove o provedor "MeuProvider" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="2dda4-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="2dda4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dda4-110">PARAMETERS</span></span>

### <span data-ttu-id="2dda4-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="2dda4-111">-Account</span></span>
<span data-ttu-id="2dda4-112">A conta do Data Lake Store para remover o provedor de identidade confiável do</span><span class="sxs-lookup"><span data-stu-id="2dda4-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="2dda4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dda4-113">-DefaultProfile</span></span>
<span data-ttu-id="2dda4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2dda4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dda4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dda4-115">-Name</span></span>
<span data-ttu-id="2dda4-116">O nome do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="2dda4-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="2dda4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dda4-117">-PassThru</span></span>
<span data-ttu-id="2dda4-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="2dda4-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dda4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dda4-119">-ResourceGroupName</span></span>
<span data-ttu-id="2dda4-120">Especifica o nome do grupo de recursos que contém a conta para remover o provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="2dda4-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="2dda4-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2dda4-121">-Confirm</span></span>
<span data-ttu-id="2dda4-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dda4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dda4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dda4-123">-WhatIf</span></span>
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

### <span data-ttu-id="2dda4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dda4-124">CommonParameters</span></span>
<span data-ttu-id="2dda4-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dda4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dda4-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dda4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dda4-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="2dda4-127">INPUTS</span></span>

### <span data-ttu-id="2dda4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2dda4-128">System.String</span></span>

### <span data-ttu-id="2dda4-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2dda4-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2dda4-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="2dda4-130">OUTPUTS</span></span>

### <span data-ttu-id="2dda4-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2dda4-131">System.Boolean</span></span>

## <span data-ttu-id="2dda4-132">Notas</span><span class="sxs-lookup"><span data-stu-id="2dda4-132">NOTES</span></span>

## <span data-ttu-id="2dda4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dda4-133">RELATED LINKS</span></span>
