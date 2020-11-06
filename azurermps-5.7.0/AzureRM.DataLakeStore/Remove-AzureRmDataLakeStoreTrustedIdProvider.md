---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c769e3e084f0ac5fd6df22bae81a4d8df99dc700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440871"
---
# <span data-ttu-id="75af7-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="75af7-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="75af7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75af7-102">SYNOPSIS</span></span>
<span data-ttu-id="75af7-103">Remove o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="75af7-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75af7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75af7-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75af7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75af7-105">DESCRIPTION</span></span>
<span data-ttu-id="75af7-106">O cmdlet **Remove-AzureRmDataLakeStoreTrustedIdProvider** remove o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="75af7-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="75af7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75af7-107">EXAMPLES</span></span>

### <span data-ttu-id="75af7-108">Exemplo 1: remover um provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="75af7-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="75af7-109">Remove o provedor "MyProvider" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="75af7-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="75af7-110">OS</span><span class="sxs-lookup"><span data-stu-id="75af7-110">PARAMETERS</span></span>

### <span data-ttu-id="75af7-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="75af7-111">-Account</span></span>
<span data-ttu-id="75af7-112">A conta do data Lake Store para remover o provedor de identidade confiável de</span><span class="sxs-lookup"><span data-stu-id="75af7-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="75af7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75af7-113">-DefaultProfile</span></span>
<span data-ttu-id="75af7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="75af7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75af7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="75af7-115">-Name</span></span>
<span data-ttu-id="75af7-116">O nome do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="75af7-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="75af7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75af7-117">-PassThru</span></span>
<span data-ttu-id="75af7-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="75af7-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="75af7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75af7-119">-ResourceGroupName</span></span>
<span data-ttu-id="75af7-120">Especifica o nome do grupo de recursos que contém a conta a partir da qual o provedor de identidade confiável será removido.</span><span class="sxs-lookup"><span data-stu-id="75af7-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="75af7-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75af7-121">-Confirm</span></span>
<span data-ttu-id="75af7-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75af7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75af7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75af7-123">-WhatIf</span></span>
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

### <span data-ttu-id="75af7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75af7-124">CommonParameters</span></span>
<span data-ttu-id="75af7-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75af7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75af7-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75af7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75af7-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75af7-127">INPUTS</span></span>

### <span data-ttu-id="75af7-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="75af7-128">None</span></span>
<span data-ttu-id="75af7-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="75af7-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75af7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75af7-130">OUTPUTS</span></span>

### <span data-ttu-id="75af7-131">bool</span><span class="sxs-lookup"><span data-stu-id="75af7-131">bool</span></span>
<span data-ttu-id="75af7-132">Se PassThru for especificado, retornará true após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="75af7-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="75af7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75af7-133">NOTES</span></span>

## <span data-ttu-id="75af7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75af7-134">RELATED LINKS</span></span>

