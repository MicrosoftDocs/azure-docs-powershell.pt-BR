---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 23f1ba9185b2a33c910afb0fc7ff0deb2a1cbf5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427954"
---
# <span data-ttu-id="be5cb-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be5cb-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="be5cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="be5cb-103">Exclui uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="be5cb-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be5cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be5cb-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be5cb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="be5cb-106">O cmdlet **Remove-AzureRmDataLakeAnalyticsAccount** exclui permanentemente uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="be5cb-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="be5cb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be5cb-107">EXAMPLES</span></span>

### <span data-ttu-id="be5cb-108">Exemplo 1: remover uma conta</span><span class="sxs-lookup"><span data-stu-id="be5cb-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="be5cb-109">Este comando Remove a conta do data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="be5cb-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="be5cb-110">OS</span><span class="sxs-lookup"><span data-stu-id="be5cb-110">PARAMETERS</span></span>

### <span data-ttu-id="be5cb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="be5cb-111">-Force</span></span>
<span data-ttu-id="be5cb-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="be5cb-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5cb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="be5cb-113">-Name</span></span>
<span data-ttu-id="be5cb-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="be5cb-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5cb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be5cb-115">-PassThru</span></span>
<span data-ttu-id="be5cb-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="be5cb-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="be5cb-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="be5cb-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="be5cb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be5cb-118">-ResourceGroupName</span></span>
<span data-ttu-id="be5cb-119">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="be5cb-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="be5cb-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="be5cb-120">-Confirm</span></span>
<span data-ttu-id="be5cb-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be5cb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be5cb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be5cb-122">-WhatIf</span></span>
<span data-ttu-id="be5cb-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be5cb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be5cb-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be5cb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be5cb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5cb-125">-DefaultProfile</span></span>
<span data-ttu-id="be5cb-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be5cb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be5cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5cb-127">CommonParameters</span></span>
<span data-ttu-id="be5cb-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5cb-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be5cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5cb-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be5cb-130">INPUTS</span></span>

## <span data-ttu-id="be5cb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be5cb-131">OUTPUTS</span></span>

### <span data-ttu-id="be5cb-132">bool</span><span class="sxs-lookup"><span data-stu-id="be5cb-132">bool</span></span>
<span data-ttu-id="be5cb-133">Se PassThru for especificado, retornará true após a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="be5cb-133">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="be5cb-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be5cb-134">NOTES</span></span>

## <span data-ttu-id="be5cb-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be5cb-135">RELATED LINKS</span></span>

[<span data-ttu-id="be5cb-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be5cb-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="be5cb-137">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be5cb-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="be5cb-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be5cb-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="be5cb-139">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="be5cb-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


