---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 089dbc5e3ca1d6a4a2a6528cb0c4bc87cf9b3dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441562"
---
# <span data-ttu-id="992ab-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="992ab-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="992ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="992ab-102">SYNOPSIS</span></span>
<span data-ttu-id="992ab-103">Remove o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="992ab-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="992ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="992ab-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="992ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="992ab-105">DESCRIPTION</span></span>
<span data-ttu-id="992ab-106">O cmdlet **Remove-AzureRmDataLakeStoreTrustedIdProvider** remove o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="992ab-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="992ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="992ab-107">EXAMPLES</span></span>

### <span data-ttu-id="992ab-108">Exemplo 1: remover um provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="992ab-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="992ab-109">Remove o provedor "MyProvider" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="992ab-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="992ab-110">OS</span><span class="sxs-lookup"><span data-stu-id="992ab-110">PARAMETERS</span></span>

### <span data-ttu-id="992ab-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="992ab-111">-Account</span></span>
<span data-ttu-id="992ab-112">A conta do data Lake Store para remover o provedor de identidade confiável de</span><span class="sxs-lookup"><span data-stu-id="992ab-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="992ab-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="992ab-113">-Name</span></span>
<span data-ttu-id="992ab-114">O nome do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="992ab-114">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="992ab-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="992ab-115">-PassThru</span></span>
<span data-ttu-id="992ab-116">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="992ab-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="992ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="992ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="992ab-118">Especifica o nome do grupo de recursos que contém a conta a partir da qual o provedor de identidade confiável será removido.</span><span class="sxs-lookup"><span data-stu-id="992ab-118">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="992ab-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="992ab-119">-Confirm</span></span>
<span data-ttu-id="992ab-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="992ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="992ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="992ab-121">-WhatIf</span></span>
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

### <span data-ttu-id="992ab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992ab-122">-DefaultProfile</span></span>
<span data-ttu-id="992ab-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="992ab-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="992ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992ab-124">CommonParameters</span></span>
<span data-ttu-id="992ab-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992ab-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="992ab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992ab-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="992ab-127">INPUTS</span></span>

## <span data-ttu-id="992ab-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="992ab-128">OUTPUTS</span></span>

### <span data-ttu-id="992ab-129">bool</span><span class="sxs-lookup"><span data-stu-id="992ab-129">bool</span></span>
<span data-ttu-id="992ab-130">Se PassThru for especificado, retornará true após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="992ab-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="992ab-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="992ab-131">NOTES</span></span>

## <span data-ttu-id="992ab-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="992ab-132">RELATED LINKS</span></span>

