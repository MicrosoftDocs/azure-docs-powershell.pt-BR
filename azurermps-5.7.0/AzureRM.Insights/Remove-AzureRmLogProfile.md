---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428916"
---
# <span data-ttu-id="85c92-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="85c92-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="85c92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85c92-102">SYNOPSIS</span></span>
<span data-ttu-id="85c92-103">Remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="85c92-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85c92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85c92-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85c92-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85c92-105">DESCRIPTION</span></span>
<span data-ttu-id="85c92-106">O cmdlet **Remove-AzureRmLogProfile** remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="85c92-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="85c92-107">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="85c92-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="85c92-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85c92-108">EXAMPLES</span></span>

## <span data-ttu-id="85c92-109">OS</span><span class="sxs-lookup"><span data-stu-id="85c92-109">PARAMETERS</span></span>

### <span data-ttu-id="85c92-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c92-110">-DefaultProfile</span></span>
<span data-ttu-id="85c92-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="85c92-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85c92-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="85c92-112">-Name</span></span>
<span data-ttu-id="85c92-113">Especifica o nome do perfil de log a ser removido.</span><span class="sxs-lookup"><span data-stu-id="85c92-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="85c92-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85c92-114">-PassThru</span></span>
<span data-ttu-id="85c92-115">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="85c92-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="85c92-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c92-116">CommonParameters</span></span>
<span data-ttu-id="85c92-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c92-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c92-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c92-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c92-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85c92-119">INPUTS</span></span>

### <span data-ttu-id="85c92-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="85c92-120">None</span></span>
<span data-ttu-id="85c92-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="85c92-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85c92-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85c92-122">OUTPUTS</span></span>

### <span data-ttu-id="85c92-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="85c92-123">AzureOperationResponse</span></span>

## <span data-ttu-id="85c92-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85c92-124">NOTES</span></span>

## <span data-ttu-id="85c92-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85c92-125">RELATED LINKS</span></span>

[<span data-ttu-id="85c92-126">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="85c92-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="85c92-127">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="85c92-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


