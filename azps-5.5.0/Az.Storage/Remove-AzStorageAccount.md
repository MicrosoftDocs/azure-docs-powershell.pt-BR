---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: e92bdaae728031ba38fc1326ac2abb29aac86c59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114411"
---
# <span data-ttu-id="9a34d-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a34d-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="9a34d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a34d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a34d-103">Remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9a34d-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="9a34d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a34d-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a34d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a34d-105">DESCRIPTION</span></span>
<span data-ttu-id="9a34d-106">O **cmdlet Remove-AzStorageAccount** remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9a34d-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="9a34d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a34d-107">EXAMPLES</span></span>

### <span data-ttu-id="9a34d-108">Exemplo 1: Remover uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9a34d-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="9a34d-109">Esse comando remove a conta de Armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="9a34d-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="9a34d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a34d-110">PARAMETERS</span></span>

### <span data-ttu-id="9a34d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a34d-111">-AsJob</span></span>
<span data-ttu-id="9a34d-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9a34d-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a34d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a34d-113">-DefaultProfile</span></span>
<span data-ttu-id="9a34d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a34d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a34d-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="9a34d-115">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a34d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a34d-116">-Name</span></span>
<span data-ttu-id="9a34d-117">Especifica o nome da conta de armazenamento a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9a34d-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a34d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a34d-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a34d-119">Especifica o nome do grupo de recursos que contém a conta de Armazenamento a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9a34d-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="9a34d-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9a34d-120">-Confirm</span></span>
<span data-ttu-id="9a34d-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a34d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a34d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a34d-122">-WhatIf</span></span>
<span data-ttu-id="9a34d-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9a34d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a34d-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a34d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a34d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a34d-125">CommonParameters</span></span>
<span data-ttu-id="9a34d-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a34d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a34d-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a34d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a34d-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="9a34d-128">INPUTS</span></span>

### <span data-ttu-id="9a34d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9a34d-129">System.String</span></span>

## <span data-ttu-id="9a34d-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="9a34d-130">OUTPUTS</span></span>

### <span data-ttu-id="9a34d-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="9a34d-131">System.Void</span></span>

## <span data-ttu-id="9a34d-132">Notas</span><span class="sxs-lookup"><span data-stu-id="9a34d-132">NOTES</span></span>

## <span data-ttu-id="9a34d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a34d-133">RELATED LINKS</span></span>

[<span data-ttu-id="9a34d-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a34d-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="9a34d-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a34d-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="9a34d-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a34d-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


