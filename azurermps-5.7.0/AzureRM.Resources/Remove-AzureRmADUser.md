---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439821"
---
# <span data-ttu-id="cbfd0-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cbfd0-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="cbfd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbfd0-102">SYNOPSIS</span></span>
<span data-ttu-id="cbfd0-103">Exclui um usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cbfd0-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbfd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbfd0-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbfd0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbfd0-105">DESCRIPTION</span></span>
<span data-ttu-id="cbfd0-106">Exclui um usuário do Active Directory (conta corporativa/de estudante também conhecida como identificação da organização).</span><span class="sxs-lookup"><span data-stu-id="cbfd0-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="cbfd0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbfd0-107">EXAMPLES</span></span>

### <span data-ttu-id="cbfd0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbfd0-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cbfd0-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="cbfd0-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="cbfd0-110">OS</span><span class="sxs-lookup"><span data-stu-id="cbfd0-110">PARAMETERS</span></span>

### <span data-ttu-id="cbfd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbfd0-111">-DefaultProfile</span></span>
<span data-ttu-id="cbfd0-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cbfd0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbfd0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cbfd0-113">-Force</span></span>
<span data-ttu-id="cbfd0-114">Se especificado, não pede confirmação para excluir o usuário.</span><span class="sxs-lookup"><span data-stu-id="cbfd0-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="cbfd0-115">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="cbfd0-115">-UPNOrObjectId</span></span>
<span data-ttu-id="cbfd0-116">O nome principal do usuário ou o objectId do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cbfd0-116">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="cbfd0-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cbfd0-117">-Confirm</span></span>
<span data-ttu-id="cbfd0-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbfd0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbfd0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbfd0-119">-WhatIf</span></span>
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

### <span data-ttu-id="cbfd0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbfd0-120">CommonParameters</span></span>
<span data-ttu-id="cbfd0-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbfd0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbfd0-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbfd0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbfd0-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbfd0-123">INPUTS</span></span>

### <span data-ttu-id="cbfd0-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cbfd0-124">None</span></span>
<span data-ttu-id="cbfd0-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cbfd0-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cbfd0-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbfd0-126">OUTPUTS</span></span>

## <span data-ttu-id="cbfd0-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbfd0-127">NOTES</span></span>

## <span data-ttu-id="cbfd0-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbfd0-128">RELATED LINKS</span></span>

[<span data-ttu-id="cbfd0-129">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cbfd0-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="cbfd0-130">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cbfd0-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="cbfd0-131">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cbfd0-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

