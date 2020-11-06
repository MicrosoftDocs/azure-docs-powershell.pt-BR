---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 5d657610ddce1c0397a5f9e8c11b832b3fcd472b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611066"
---
# <span data-ttu-id="75227-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75227-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="75227-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75227-102">SYNOPSIS</span></span>
<span data-ttu-id="75227-103">Exclui um usuário existente.</span><span class="sxs-lookup"><span data-stu-id="75227-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75227-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75227-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75227-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75227-105">DESCRIPTION</span></span>
<span data-ttu-id="75227-106">O cmdlet **Remove-AzureRmApiManagementUser** exclui um usuário existente.</span><span class="sxs-lookup"><span data-stu-id="75227-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="75227-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75227-107">EXAMPLES</span></span>

### <span data-ttu-id="75227-108">Exemplo 1: excluir um usuário</span><span class="sxs-lookup"><span data-stu-id="75227-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="75227-109">Esse comando exclui um usuário existente.</span><span class="sxs-lookup"><span data-stu-id="75227-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="75227-110">OS</span><span class="sxs-lookup"><span data-stu-id="75227-110">PARAMETERS</span></span>

### <span data-ttu-id="75227-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="75227-111">-Context</span></span>
<span data-ttu-id="75227-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="75227-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="75227-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="75227-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75227-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75227-114">-DefaultProfile</span></span>
<span data-ttu-id="75227-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75227-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="75227-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="75227-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="75227-117">Indica se as assinaturas devem ser excluídas do produto.</span><span class="sxs-lookup"><span data-stu-id="75227-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="75227-118">Se esse parâmetro não for especificado e houver uma assinatura, esse cmdlet lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="75227-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="75227-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="75227-119">This parameter is optional.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75227-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75227-120">-PassThru</span></span>
<span data-ttu-id="75227-121">Indica que esse cmdlet retorna um valor de $Ture, se tiver êxito, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="75227-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75227-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="75227-122">-UserId</span></span>
<span data-ttu-id="75227-123">Especifica a ID do usuário a ser removida.</span><span class="sxs-lookup"><span data-stu-id="75227-123">Specifies the ID of the user to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75227-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75227-124">-Confirm</span></span>
<span data-ttu-id="75227-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75227-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75227-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75227-126">-WhatIf</span></span>
<span data-ttu-id="75227-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75227-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75227-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75227-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75227-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75227-129">CommonParameters</span></span>
<span data-ttu-id="75227-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75227-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75227-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75227-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75227-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75227-132">INPUTS</span></span>

### <span data-ttu-id="75227-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="75227-133">None</span></span>
<span data-ttu-id="75227-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="75227-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75227-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75227-135">OUTPUTS</span></span>

### <span data-ttu-id="75227-136">Booliana</span><span class="sxs-lookup"><span data-stu-id="75227-136">Boolean</span></span>

## <span data-ttu-id="75227-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75227-137">NOTES</span></span>

## <span data-ttu-id="75227-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75227-138">RELATED LINKS</span></span>

[<span data-ttu-id="75227-139">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75227-139">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="75227-140">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75227-140">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="75227-141">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75227-141">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


