---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 2ee08eaf9dae9a6d2001608d8ef247c7e116c98e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428945"
---
# <span data-ttu-id="3d35e-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="3d35e-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="3d35e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d35e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d35e-103">Exclui um segredo de análise do data Lake.</span><span class="sxs-lookup"><span data-stu-id="3d35e-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d35e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d35e-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d35e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d35e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d35e-106">O cmdlet **Remove-AzureRmDataLakeAnalyticsCatalogSecret** exclui um segredo de catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3d35e-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="3d35e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d35e-107">EXAMPLES</span></span>

### <span data-ttu-id="3d35e-108">Exemplo 1: remover um segredo</span><span class="sxs-lookup"><span data-stu-id="3d35e-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="3d35e-109">Este comando Remove o segredo especificado do catálogo do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3d35e-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="3d35e-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d35e-110">PARAMETERS</span></span>

### <span data-ttu-id="3d35e-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="3d35e-111">-Account</span></span>
<span data-ttu-id="3d35e-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3d35e-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3d35e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d35e-113">-DatabaseName</span></span>
<span data-ttu-id="3d35e-114">Especifica o nome do banco de dados que contém o segredo.</span><span class="sxs-lookup"><span data-stu-id="3d35e-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="3d35e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d35e-115">-DefaultProfile</span></span>
<span data-ttu-id="3d35e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3d35e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d35e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3d35e-117">-Force</span></span>
<span data-ttu-id="3d35e-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3d35e-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d35e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d35e-119">-Name</span></span>
<span data-ttu-id="3d35e-120">Especifica o nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="3d35e-120">Specifies the name of the secret.</span></span>

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

### <span data-ttu-id="3d35e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d35e-121">-PassThru</span></span>
<span data-ttu-id="3d35e-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3d35e-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3d35e-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3d35e-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d35e-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d35e-124">-Confirm</span></span>
<span data-ttu-id="3d35e-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d35e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d35e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d35e-126">-WhatIf</span></span>
<span data-ttu-id="3d35e-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d35e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d35e-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d35e-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d35e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d35e-129">CommonParameters</span></span>
<span data-ttu-id="3d35e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d35e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d35e-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d35e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d35e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d35e-132">INPUTS</span></span>

### <span data-ttu-id="3d35e-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3d35e-133">None</span></span>
<span data-ttu-id="3d35e-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3d35e-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d35e-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d35e-135">OUTPUTS</span></span>

### <span data-ttu-id="3d35e-136">bool</span><span class="sxs-lookup"><span data-stu-id="3d35e-136">bool</span></span>
<span data-ttu-id="3d35e-137">Se PassThru for especificado, retornará true após a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="3d35e-137">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="3d35e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d35e-138">NOTES</span></span>

## <span data-ttu-id="3d35e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d35e-139">RELATED LINKS</span></span>

[<span data-ttu-id="3d35e-140">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="3d35e-140">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="3d35e-141">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="3d35e-141">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)

