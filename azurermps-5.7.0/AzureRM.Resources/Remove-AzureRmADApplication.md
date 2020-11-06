---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603225"
---
# <span data-ttu-id="ea376-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ea376-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="ea376-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea376-102">SYNOPSIS</span></span>
<span data-ttu-id="ea376-103">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea376-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea376-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea376-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea376-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea376-105">DESCRIPTION</span></span>
<span data-ttu-id="ea376-106">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea376-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="ea376-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea376-107">EXAMPLES</span></span>

### <span data-ttu-id="ea376-108">Exclua o aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="ea376-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="ea376-109">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea376-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="ea376-110">OS</span><span class="sxs-lookup"><span data-stu-id="ea376-110">PARAMETERS</span></span>

### <span data-ttu-id="ea376-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea376-111">-DefaultProfile</span></span>
<span data-ttu-id="ea376-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ea376-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea376-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ea376-113">-Force</span></span>
<span data-ttu-id="ea376-114">Alternar para excluir um aplicativo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="ea376-114">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="ea376-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ea376-115">-ObjectId</span></span>
<span data-ttu-id="ea376-116">A ID do objeto do aplicativo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="ea376-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea376-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea376-117">-Confirm</span></span>
<span data-ttu-id="ea376-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea376-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea376-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea376-119">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea376-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea376-120">CommonParameters</span></span>
<span data-ttu-id="ea376-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea376-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea376-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea376-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea376-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea376-123">INPUTS</span></span>

### <span data-ttu-id="ea376-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ea376-124">None</span></span>
<span data-ttu-id="ea376-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ea376-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea376-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea376-126">OUTPUTS</span></span>

## <span data-ttu-id="ea376-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea376-127">NOTES</span></span>
<span data-ttu-id="ea376-128">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="ea376-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ea376-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea376-129">RELATED LINKS</span></span>

[<span data-ttu-id="ea376-130">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ea376-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="ea376-131">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ea376-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="ea376-132">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ea376-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="ea376-133">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ea376-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

