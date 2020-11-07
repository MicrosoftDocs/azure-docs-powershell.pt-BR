---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: eb30f07e0443712e7287ae850f463070f5aca3f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777260"
---
# <span data-ttu-id="a5a1b-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a5a1b-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="a5a1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a1b-103">Obtém detalhes de uma conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="a5a1b-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="a5a1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5a1b-104">SYNTAX</span></span>

### <span data-ttu-id="a5a1b-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5a1b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5a1b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a1b-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a1b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5a1b-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a1b-108">O cmdlet **Get-AzNetAppFilesAccount** Obtém detalhes de uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="a5a1b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5a1b-109">EXAMPLES</span></span>

### <span data-ttu-id="a5a1b-110">Exemplo 1: obter uma conta do ANF</span><span class="sxs-lookup"><span data-stu-id="a5a1b-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="a5a1b-111">Esse comando obtém a conta chamada MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="a5a1b-112">OS</span><span class="sxs-lookup"><span data-stu-id="a5a1b-112">PARAMETERS</span></span>

### <span data-ttu-id="a5a1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a1b-113">-DefaultProfile</span></span>
<span data-ttu-id="a5a1b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5a1b-115">-Name</span></span>
<span data-ttu-id="a5a1b-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="a5a1b-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a1b-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5a1b-118">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="a5a1b-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5a1b-119">-ResourceId</span></span>
<span data-ttu-id="a5a1b-120">A ID do recurso da conta ANF</span><span class="sxs-lookup"><span data-stu-id="a5a1b-120">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a1b-121">CommonParameters</span></span>
<span data-ttu-id="a5a1b-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a5a1b-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a1b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a1b-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5a1b-124">INPUTS</span></span>

### <span data-ttu-id="a5a1b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a1b-125">System.String</span></span>

## <span data-ttu-id="a5a1b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5a1b-126">OUTPUTS</span></span>

### <span data-ttu-id="a5a1b-127">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a5a1b-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a5a1b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5a1b-128">NOTES</span></span>

## <span data-ttu-id="a5a1b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5a1b-129">RELATED LINKS</span></span>
