---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432629"
---
# <span data-ttu-id="aa6b6-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="aa6b6-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="aa6b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa6b6-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6b6-103">Exclui uma conta do data Lake Store permanentemente.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa6b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa6b6-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa6b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa6b6-105">DESCRIPTION</span></span>
<span data-ttu-id="aa6b6-106">O cmdlet **Remove-AzureRmDataLakeStoreAccount** exclui uma conta do data Lake Store permanentemente.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="aa6b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa6b6-107">EXAMPLES</span></span>

### <span data-ttu-id="aa6b6-108">Exemplo 1: remover uma conta do data Lake Store</span><span class="sxs-lookup"><span data-stu-id="aa6b6-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="aa6b6-109">Esse comando Remove a conta chamada ContosoADL do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="aa6b6-110">OS</span><span class="sxs-lookup"><span data-stu-id="aa6b6-110">PARAMETERS</span></span>

### <span data-ttu-id="aa6b6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="aa6b6-111">-Force</span></span>
<span data-ttu-id="aa6b6-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa6b6-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa6b6-113">-Name</span></span>
<span data-ttu-id="aa6b6-114">Especifica o nome da conta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-114">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="aa6b6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa6b6-115">-PassThru</span></span>
<span data-ttu-id="aa6b6-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aa6b6-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa6b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa6b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="aa6b6-119">Especifica o grupo de recursos que contém a conta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-119">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="aa6b6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa6b6-120">-Confirm</span></span>
<span data-ttu-id="aa6b6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa6b6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa6b6-122">-WhatIf</span></span>
<span data-ttu-id="aa6b6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa6b6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa6b6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa6b6-125">-DefaultProfile</span></span>
<span data-ttu-id="aa6b6-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa6b6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6b6-127">CommonParameters</span></span>
<span data-ttu-id="aa6b6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6b6-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa6b6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6b6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa6b6-130">INPUTS</span></span>

## <span data-ttu-id="aa6b6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa6b6-131">OUTPUTS</span></span>

### <span data-ttu-id="aa6b6-132">bool</span><span class="sxs-lookup"><span data-stu-id="aa6b6-132">bool</span></span>
<span data-ttu-id="aa6b6-133">Se PassThru for especificado, retornará true após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="aa6b6-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="aa6b6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa6b6-134">NOTES</span></span>

## <span data-ttu-id="aa6b6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa6b6-135">RELATED LINKS</span></span>

[<span data-ttu-id="aa6b6-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="aa6b6-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="aa6b6-137">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="aa6b6-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="aa6b6-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="aa6b6-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="aa6b6-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="aa6b6-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


