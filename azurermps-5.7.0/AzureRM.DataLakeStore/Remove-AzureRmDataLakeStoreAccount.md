---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 4e21d122c8a49209a7591457c36ba99fcc10496c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427560"
---
# <span data-ttu-id="7e5e7-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e5e7-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="7e5e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5e7-103">Exclui uma conta do data Lake Store permanentemente.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e5e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e5e7-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e5e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e5e7-105">DESCRIPTION</span></span>
<span data-ttu-id="7e5e7-106">O cmdlet **Remove-AzureRmDataLakeStoreAccount** exclui uma conta do data Lake Store permanentemente.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="7e5e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e5e7-107">EXAMPLES</span></span>

### <span data-ttu-id="7e5e7-108">Exemplo 1: remover uma conta do data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7e5e7-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="7e5e7-109">Esse comando Remove a conta chamada ContosoADL do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="7e5e7-110">OS</span><span class="sxs-lookup"><span data-stu-id="7e5e7-110">PARAMETERS</span></span>

### <span data-ttu-id="7e5e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5e7-111">-DefaultProfile</span></span>
<span data-ttu-id="7e5e7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7e5e7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e5e7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7e5e7-113">-Force</span></span>
<span data-ttu-id="7e5e7-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e5e7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e5e7-115">-Name</span></span>
<span data-ttu-id="7e5e7-116">Especifica o nome da conta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="7e5e7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e5e7-117">-PassThru</span></span>
<span data-ttu-id="7e5e7-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7e5e7-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e5e7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5e7-120">-ResourceGroupName</span></span>
<span data-ttu-id="7e5e7-121">Especifica o grupo de recursos que contém a conta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="7e5e7-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e5e7-122">-Confirm</span></span>
<span data-ttu-id="7e5e7-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e5e7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e5e7-124">-WhatIf</span></span>
<span data-ttu-id="7e5e7-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e5e7-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e5e7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5e7-127">CommonParameters</span></span>
<span data-ttu-id="7e5e7-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5e7-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e5e7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5e7-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e5e7-130">INPUTS</span></span>

### <span data-ttu-id="7e5e7-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7e5e7-131">None</span></span>
<span data-ttu-id="7e5e7-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e5e7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e5e7-133">OUTPUTS</span></span>

### <span data-ttu-id="7e5e7-134">bool</span><span class="sxs-lookup"><span data-stu-id="7e5e7-134">bool</span></span>
<span data-ttu-id="7e5e7-135">Se PassThru for especificado, retornará true após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7e5e7-135">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="7e5e7-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e5e7-136">NOTES</span></span>

## <span data-ttu-id="7e5e7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e5e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="7e5e7-138">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e5e7-138">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7e5e7-139">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e5e7-139">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7e5e7-140">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e5e7-140">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7e5e7-141">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e5e7-141">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


