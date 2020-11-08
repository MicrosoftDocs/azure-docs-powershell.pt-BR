---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112751"
---
# <span data-ttu-id="0855a-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="0855a-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="0855a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0855a-102">SYNOPSIS</span></span>
<span data-ttu-id="0855a-103">Retorna as chaves BitLocker para todas as unidades no trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="0855a-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="0855a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0855a-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0855a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0855a-105">DESCRIPTION</span></span>
<span data-ttu-id="0855a-106">Retorna as chaves BitLocker para todas as unidades no trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="0855a-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="0855a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0855a-107">EXAMPLES</span></span>

### <span data-ttu-id="0855a-108">Exemplo 1: listar todas as chaves do BitLocker no trabalho ImportExport especificado</span><span class="sxs-lookup"><span data-stu-id="0855a-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="0855a-109">Esse cmdlet lista todas as chaves do BitLocker no trabalho ImportExport especificado.</span><span class="sxs-lookup"><span data-stu-id="0855a-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="0855a-110">OS</span><span class="sxs-lookup"><span data-stu-id="0855a-110">PARAMETERS</span></span>

### <span data-ttu-id="0855a-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="0855a-111">-AcceptLanguage</span></span>
<span data-ttu-id="0855a-112">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="0855a-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="0855a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0855a-113">-DefaultProfile</span></span>
<span data-ttu-id="0855a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0855a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0855a-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="0855a-115">-JobName</span></span>
<span data-ttu-id="0855a-116">O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="0855a-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="0855a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0855a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0855a-118">O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="0855a-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="0855a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0855a-119">-SubscriptionId</span></span>
<span data-ttu-id="0855a-120">A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="0855a-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="0855a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0855a-121">CommonParameters</span></span>
<span data-ttu-id="0855a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0855a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0855a-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0855a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0855a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0855a-124">INPUTS</span></span>

## <span data-ttu-id="0855a-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0855a-125">OUTPUTS</span></span>

### <span data-ttu-id="0855a-126">Microsoft. Azure. PowerShell. cmdlets. ImportExport. Models. Api20161101. IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="0855a-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="0855a-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0855a-127">NOTES</span></span>

<span data-ttu-id="0855a-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0855a-128">ALIASES</span></span>

## <span data-ttu-id="0855a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0855a-129">RELATED LINKS</span></span>

