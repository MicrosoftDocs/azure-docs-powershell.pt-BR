---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3276a23869633238ebc6b84dfa01934e5ad9896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425754"
---
# <span data-ttu-id="40d61-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40d61-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="40d61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40d61-102">SYNOPSIS</span></span>
<span data-ttu-id="40d61-103">Remove uma política de acesso armazenado de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="40d61-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="40d61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40d61-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d61-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40d61-105">DESCRIPTION</span></span>
<span data-ttu-id="40d61-106">O cmdlet **Remove-AzureStorageTableStoredAccessPolicy** remove uma política de acesso armazenado de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="40d61-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="40d61-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40d61-107">EXAMPLES</span></span>

### <span data-ttu-id="40d61-108">Exemplo 1: remover uma política de acesso armazenado de uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="40d61-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="40d61-109">Esse comando Remove a política denominada Policy05 da tabela de armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="40d61-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="40d61-110">OS</span><span class="sxs-lookup"><span data-stu-id="40d61-110">PARAMETERS</span></span>

### <span data-ttu-id="40d61-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="40d61-111">-Context</span></span>
<span data-ttu-id="40d61-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="40d61-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="40d61-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="40d61-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40d61-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40d61-114">-PassThru</span></span>
<span data-ttu-id="40d61-115">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="40d61-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="40d61-116">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="40d61-116">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d61-117">-Política</span><span class="sxs-lookup"><span data-stu-id="40d61-117">-Policy</span></span>
<span data-ttu-id="40d61-118">Especifica a política de acesso armazenada, que inclui as permissões para este token SAS.</span><span class="sxs-lookup"><span data-stu-id="40d61-118">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="40d61-119">-Tabela</span><span class="sxs-lookup"><span data-stu-id="40d61-119">-Table</span></span>
<span data-ttu-id="40d61-120">Especifica o nome da tabela do Azure.</span><span class="sxs-lookup"><span data-stu-id="40d61-120">Specifies the Azure table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d61-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40d61-121">-Confirm</span></span>
<span data-ttu-id="40d61-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d61-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d61-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d61-123">-WhatIf</span></span>
<span data-ttu-id="40d61-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40d61-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d61-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40d61-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d61-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d61-126">CommonParameters</span></span>
<span data-ttu-id="40d61-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d61-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d61-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d61-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d61-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40d61-129">INPUTS</span></span>

## <span data-ttu-id="40d61-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40d61-130">OUTPUTS</span></span>

## <span data-ttu-id="40d61-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40d61-131">NOTES</span></span>

## <span data-ttu-id="40d61-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40d61-132">RELATED LINKS</span></span>

[<span data-ttu-id="40d61-133">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40d61-133">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="40d61-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="40d61-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="40d61-135">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40d61-135">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="40d61-136">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40d61-136">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
