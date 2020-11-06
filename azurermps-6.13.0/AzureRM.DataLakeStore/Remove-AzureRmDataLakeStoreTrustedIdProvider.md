---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f281192e22cd8acdf85e389d82ef7146590be158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426362"
---
# <span data-ttu-id="df5cc-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="df5cc-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="df5cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="df5cc-103">Remove o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="df5cc-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df5cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df5cc-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df5cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df5cc-105">DESCRIPTION</span></span>
<span data-ttu-id="df5cc-106">O cmdlet **Remove-AzureRmDataLakeStoreTrustedIdProvider** remove o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="df5cc-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="df5cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df5cc-107">EXAMPLES</span></span>

### <span data-ttu-id="df5cc-108">Exemplo 1: remover um provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="df5cc-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="df5cc-109">Remove o provedor "MyProvider" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="df5cc-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="df5cc-110">OS</span><span class="sxs-lookup"><span data-stu-id="df5cc-110">PARAMETERS</span></span>

### <span data-ttu-id="df5cc-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="df5cc-111">-Account</span></span>
<span data-ttu-id="df5cc-112">A conta do data Lake Store para remover o provedor de identidade confiável de</span><span class="sxs-lookup"><span data-stu-id="df5cc-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="df5cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5cc-113">-DefaultProfile</span></span>
<span data-ttu-id="df5cc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="df5cc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df5cc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="df5cc-115">-Name</span></span>
<span data-ttu-id="df5cc-116">O nome do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="df5cc-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="df5cc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df5cc-117">-PassThru</span></span>
<span data-ttu-id="df5cc-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="df5cc-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="df5cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="df5cc-120">Especifica o nome do grupo de recursos que contém a conta a partir da qual o provedor de identidade confiável será removido.</span><span class="sxs-lookup"><span data-stu-id="df5cc-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="df5cc-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df5cc-121">-Confirm</span></span>
<span data-ttu-id="df5cc-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df5cc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df5cc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df5cc-123">-WhatIf</span></span>
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

### <span data-ttu-id="df5cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5cc-124">CommonParameters</span></span>
<span data-ttu-id="df5cc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5cc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5cc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5cc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df5cc-127">INPUTS</span></span>

### <span data-ttu-id="df5cc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="df5cc-128">System.String</span></span>

### <span data-ttu-id="df5cc-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df5cc-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df5cc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df5cc-130">OUTPUTS</span></span>

### <span data-ttu-id="df5cc-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df5cc-131">System.Boolean</span></span>

## <span data-ttu-id="df5cc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df5cc-132">NOTES</span></span>

## <span data-ttu-id="df5cc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df5cc-133">RELATED LINKS</span></span>
