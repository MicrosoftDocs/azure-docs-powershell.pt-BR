---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111760"
---
# <span data-ttu-id="8e85c-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e85c-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="8e85c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e85c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e85c-103">Obtém um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="8e85c-103">Gets a log profile.</span></span>

## <span data-ttu-id="8e85c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e85c-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e85c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e85c-105">DESCRIPTION</span></span>
<span data-ttu-id="8e85c-106">O **cmdlet Get-AzLogProfile** obtém um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="8e85c-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="8e85c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e85c-107">EXAMPLES</span></span>

## <span data-ttu-id="8e85c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e85c-108">PARAMETERS</span></span>

### <span data-ttu-id="8e85c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e85c-109">-DefaultProfile</span></span>
<span data-ttu-id="8e85c-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8e85c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e85c-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e85c-111">-Name</span></span>
<span data-ttu-id="8e85c-112">Especifica o nome do perfil de log a ser obter.</span><span class="sxs-lookup"><span data-stu-id="8e85c-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e85c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e85c-113">CommonParameters</span></span>
<span data-ttu-id="8e85c-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e85c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e85c-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e85c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e85c-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e85c-116">INPUTS</span></span>

### <span data-ttu-id="8e85c-117">System.String</span><span class="sxs-lookup"><span data-stu-id="8e85c-117">System.String</span></span>

## <span data-ttu-id="8e85c-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e85c-118">OUTPUTS</span></span>

### <span data-ttu-id="8e85c-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="8e85c-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="8e85c-120">Notas</span><span class="sxs-lookup"><span data-stu-id="8e85c-120">NOTES</span></span>

## <span data-ttu-id="8e85c-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e85c-121">RELATED LINKS</span></span>

[<span data-ttu-id="8e85c-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e85c-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="8e85c-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e85c-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


