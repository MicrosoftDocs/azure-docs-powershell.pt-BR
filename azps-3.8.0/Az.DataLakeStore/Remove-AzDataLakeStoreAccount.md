---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777773"
---
# <span data-ttu-id="dbaa6-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbaa6-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="dbaa6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbaa6-103">Exclui uma conta do data Lake Store permanentemente.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="dbaa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbaa6-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbaa6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbaa6-105">DESCRIPTION</span></span>
<span data-ttu-id="dbaa6-106">O cmdlet **Remove-AzDataLakeStoreAccount** exclui uma conta do data Lake Store permanentemente.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="dbaa6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbaa6-107">EXAMPLES</span></span>

### <span data-ttu-id="dbaa6-108">Exemplo 1: remover uma conta do data Lake Store</span><span class="sxs-lookup"><span data-stu-id="dbaa6-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="dbaa6-109">Esse comando Remove a conta chamada ContosoADL do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="dbaa6-110">OS</span><span class="sxs-lookup"><span data-stu-id="dbaa6-110">PARAMETERS</span></span>

### <span data-ttu-id="dbaa6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbaa6-111">-DefaultProfile</span></span>
<span data-ttu-id="dbaa6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dbaa6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbaa6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dbaa6-113">-Force</span></span>
<span data-ttu-id="dbaa6-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbaa6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbaa6-115">-Name</span></span>
<span data-ttu-id="dbaa6-116">Especifica o nome da conta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="dbaa6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbaa6-117">-PassThru</span></span>
<span data-ttu-id="dbaa6-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dbaa6-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbaa6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbaa6-120">-ResourceGroupName</span></span>
<span data-ttu-id="dbaa6-121">Especifica o grupo de recursos que contém a conta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="dbaa6-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dbaa6-122">-Confirm</span></span>
<span data-ttu-id="dbaa6-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbaa6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbaa6-124">-WhatIf</span></span>
<span data-ttu-id="dbaa6-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbaa6-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbaa6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbaa6-127">CommonParameters</span></span>
<span data-ttu-id="dbaa6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbaa6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbaa6-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbaa6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbaa6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbaa6-130">INPUTS</span></span>

### <span data-ttu-id="dbaa6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dbaa6-131">System.String</span></span>

## <span data-ttu-id="dbaa6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbaa6-132">OUTPUTS</span></span>

### <span data-ttu-id="dbaa6-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbaa6-133">System.Boolean</span></span>

## <span data-ttu-id="dbaa6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbaa6-134">NOTES</span></span>

## <span data-ttu-id="dbaa6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbaa6-135">RELATED LINKS</span></span>

[<span data-ttu-id="dbaa6-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbaa6-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dbaa6-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbaa6-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dbaa6-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbaa6-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dbaa6-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbaa6-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


