---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: f978925766fb664f5ddeaf3b6dffa94e55244f43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602375"
---
# <span data-ttu-id="8c999-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8c999-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="8c999-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c999-102">SYNOPSIS</span></span>
<span data-ttu-id="8c999-103">Exclui uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c999-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c999-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c999-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c999-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c999-105">DESCRIPTION</span></span>
<span data-ttu-id="8c999-106">O cmdlet **Remove-AzureRmDataLakeAnalyticsAccount** exclui permanentemente uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c999-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8c999-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c999-107">EXAMPLES</span></span>

### <span data-ttu-id="8c999-108">Exemplo 1: remover uma conta</span><span class="sxs-lookup"><span data-stu-id="8c999-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="8c999-109">Este comando Remove a conta do data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="8c999-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="8c999-110">OS</span><span class="sxs-lookup"><span data-stu-id="8c999-110">PARAMETERS</span></span>

### <span data-ttu-id="8c999-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c999-111">-DefaultProfile</span></span>
<span data-ttu-id="8c999-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8c999-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c999-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8c999-113">-Force</span></span>
<span data-ttu-id="8c999-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c999-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c999-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c999-115">-Name</span></span>
<span data-ttu-id="8c999-116">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c999-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c999-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c999-117">-PassThru</span></span>
<span data-ttu-id="8c999-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8c999-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c999-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8c999-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c999-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c999-120">-ResourceGroupName</span></span>
<span data-ttu-id="8c999-121">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c999-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="8c999-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c999-122">-Confirm</span></span>
<span data-ttu-id="8c999-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c999-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c999-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c999-124">-WhatIf</span></span>
<span data-ttu-id="8c999-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c999-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c999-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c999-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c999-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c999-127">CommonParameters</span></span>
<span data-ttu-id="8c999-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c999-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c999-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c999-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c999-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c999-130">INPUTS</span></span>

### <span data-ttu-id="8c999-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8c999-131">None</span></span>
<span data-ttu-id="8c999-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8c999-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c999-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c999-133">OUTPUTS</span></span>

### <span data-ttu-id="8c999-134">bool</span><span class="sxs-lookup"><span data-stu-id="8c999-134">bool</span></span>
<span data-ttu-id="8c999-135">Se PassThru for especificado, retornará true após a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="8c999-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="8c999-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c999-136">NOTES</span></span>

## <span data-ttu-id="8c999-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c999-137">RELATED LINKS</span></span>

[<span data-ttu-id="8c999-138">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8c999-138">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8c999-139">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8c999-139">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8c999-140">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8c999-140">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8c999-141">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8c999-141">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


