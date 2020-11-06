---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 16716b0df5867832d51ed00797f19d5dfc0f0b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609715"
---
# <span data-ttu-id="2f23b-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="2f23b-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="2f23b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f23b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f23b-103">Exclui um segredo de análise do data Lake.</span><span class="sxs-lookup"><span data-stu-id="2f23b-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f23b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f23b-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f23b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f23b-105">DESCRIPTION</span></span>
<span data-ttu-id="2f23b-106">O cmdlet **Remove-AzureRmDataLakeAnalyticsCatalogSecret** exclui um segredo de catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2f23b-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="2f23b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f23b-107">EXAMPLES</span></span>

### <span data-ttu-id="2f23b-108">Exemplo 1: remover um segredo</span><span class="sxs-lookup"><span data-stu-id="2f23b-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="2f23b-109">Este comando Remove o segredo especificado do catálogo do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2f23b-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="2f23b-110">OS</span><span class="sxs-lookup"><span data-stu-id="2f23b-110">PARAMETERS</span></span>

### <span data-ttu-id="2f23b-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="2f23b-111">-Account</span></span>
<span data-ttu-id="2f23b-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2f23b-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2f23b-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f23b-113">-DatabaseName</span></span>
<span data-ttu-id="2f23b-114">Especifica o nome do banco de dados que contém o segredo.</span><span class="sxs-lookup"><span data-stu-id="2f23b-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="2f23b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2f23b-115">-Force</span></span>
<span data-ttu-id="2f23b-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2f23b-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f23b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f23b-117">-Name</span></span>
<span data-ttu-id="2f23b-118">Especifica o nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="2f23b-118">Specifies the name of the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f23b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f23b-119">-PassThru</span></span>
<span data-ttu-id="2f23b-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2f23b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f23b-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="2f23b-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f23b-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f23b-122">-Confirm</span></span>
<span data-ttu-id="2f23b-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f23b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f23b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f23b-124">-WhatIf</span></span>
<span data-ttu-id="2f23b-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f23b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f23b-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f23b-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f23b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f23b-127">-DefaultProfile</span></span>
<span data-ttu-id="2f23b-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f23b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f23b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f23b-129">CommonParameters</span></span>
<span data-ttu-id="2f23b-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f23b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f23b-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f23b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f23b-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f23b-132">INPUTS</span></span>

## <span data-ttu-id="2f23b-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f23b-133">OUTPUTS</span></span>

### <span data-ttu-id="2f23b-134">bool</span><span class="sxs-lookup"><span data-stu-id="2f23b-134">bool</span></span>
<span data-ttu-id="2f23b-135">Se PassThru for especificado, retornará true após a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="2f23b-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="2f23b-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f23b-136">NOTES</span></span>

## <span data-ttu-id="2f23b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f23b-137">RELATED LINKS</span></span>

[<span data-ttu-id="2f23b-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="2f23b-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="2f23b-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="2f23b-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


