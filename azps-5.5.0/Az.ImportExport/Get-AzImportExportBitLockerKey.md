---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118972"
---
# <span data-ttu-id="35b45-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="35b45-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="35b45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35b45-102">SYNOPSIS</span></span>
<span data-ttu-id="35b45-103">Retorna as Teclas BitLocker para todas as unidades no trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="35b45-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="35b45-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35b45-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="35b45-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="35b45-105">DESCRIPTION</span></span>
<span data-ttu-id="35b45-106">Retorna as Teclas BitLocker para todas as unidades no trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="35b45-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="35b45-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35b45-107">EXAMPLES</span></span>

### <span data-ttu-id="35b45-108">Exemplo 1: Listar todas as Chaves do BitLocker no trabalho ImportExport especificado</span><span class="sxs-lookup"><span data-stu-id="35b45-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="35b45-109">Este cmdlet lista todas as Teclas BitLocker no trabalho ImportExport especificado.</span><span class="sxs-lookup"><span data-stu-id="35b45-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="35b45-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35b45-110">PARAMETERS</span></span>

### <span data-ttu-id="35b45-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="35b45-111">-AcceptLanguage</span></span>
<span data-ttu-id="35b45-112">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="35b45-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b45-113">-DefaultProfile</span></span>
<span data-ttu-id="35b45-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35b45-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b45-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="35b45-115">-JobName</span></span>
<span data-ttu-id="35b45-116">O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="35b45-116">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b45-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35b45-117">-ResourceGroupName</span></span>
<span data-ttu-id="35b45-118">O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="35b45-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b45-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35b45-119">-SubscriptionId</span></span>
<span data-ttu-id="35b45-120">A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="35b45-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b45-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b45-121">CommonParameters</span></span>
<span data-ttu-id="35b45-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b45-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b45-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35b45-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b45-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="35b45-124">INPUTS</span></span>

## <span data-ttu-id="35b45-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="35b45-125">OUTPUTS</span></span>

### <span data-ttu-id="35b45-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="35b45-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="35b45-127">Notas</span><span class="sxs-lookup"><span data-stu-id="35b45-127">NOTES</span></span>

<span data-ttu-id="35b45-128">Aliases</span><span class="sxs-lookup"><span data-stu-id="35b45-128">ALIASES</span></span>

## <span data-ttu-id="35b45-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35b45-129">RELATED LINKS</span></span>

