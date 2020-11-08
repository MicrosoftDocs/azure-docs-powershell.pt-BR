---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112514"
---
# <span data-ttu-id="23fc6-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="23fc6-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="23fc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="23fc6-103">Remove o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="23fc6-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="23fc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23fc6-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23fc6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="23fc6-106">O cmdlet **Remove-AzDataLakeStoreTrustedIdProvider** remove o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="23fc6-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="23fc6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="23fc6-108">Exemplo 1: remover um provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="23fc6-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="23fc6-109">Remove o provedor "MyProvider" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="23fc6-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="23fc6-110">OS</span><span class="sxs-lookup"><span data-stu-id="23fc6-110">PARAMETERS</span></span>

### <span data-ttu-id="23fc6-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="23fc6-111">-Account</span></span>
<span data-ttu-id="23fc6-112">A conta do data Lake Store para remover o provedor de identidade confiável de</span><span class="sxs-lookup"><span data-stu-id="23fc6-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="23fc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fc6-113">-DefaultProfile</span></span>
<span data-ttu-id="23fc6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="23fc6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23fc6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="23fc6-115">-Name</span></span>
<span data-ttu-id="23fc6-116">O nome do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="23fc6-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="23fc6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23fc6-117">-PassThru</span></span>
<span data-ttu-id="23fc6-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="23fc6-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="23fc6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23fc6-119">-ResourceGroupName</span></span>
<span data-ttu-id="23fc6-120">Especifica o nome do grupo de recursos que contém a conta a partir da qual o provedor de identidade confiável será removido.</span><span class="sxs-lookup"><span data-stu-id="23fc6-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="23fc6-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23fc6-121">-Confirm</span></span>
<span data-ttu-id="23fc6-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23fc6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23fc6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23fc6-123">-WhatIf</span></span>
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

### <span data-ttu-id="23fc6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fc6-124">CommonParameters</span></span>
<span data-ttu-id="23fc6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23fc6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fc6-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fc6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fc6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23fc6-127">INPUTS</span></span>

### <span data-ttu-id="23fc6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="23fc6-128">System.String</span></span>

### <span data-ttu-id="23fc6-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23fc6-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23fc6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23fc6-130">OUTPUTS</span></span>

### <span data-ttu-id="23fc6-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23fc6-131">System.Boolean</span></span>

## <span data-ttu-id="23fc6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23fc6-132">NOTES</span></span>

## <span data-ttu-id="23fc6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23fc6-133">RELATED LINKS</span></span>
