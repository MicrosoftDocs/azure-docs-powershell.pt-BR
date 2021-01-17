---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427078"
---
# <span data-ttu-id="bb82f-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bb82f-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="bb82f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb82f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb82f-103">Obtém detalhes de uma conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="bb82f-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="bb82f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb82f-104">SYNTAX</span></span>

### <span data-ttu-id="bb82f-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb82f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb82f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb82f-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb82f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb82f-107">DESCRIPTION</span></span>
<span data-ttu-id="bb82f-108">O cmdlet **Get-AzNetAppFilesAccount** Obtém detalhes de uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="bb82f-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="bb82f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb82f-109">EXAMPLES</span></span>

### <span data-ttu-id="bb82f-110">Exemplo 1: obter uma conta do ANF</span><span class="sxs-lookup"><span data-stu-id="bb82f-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="bb82f-111">Esse comando obtém a conta chamada MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="bb82f-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="bb82f-112">OS</span><span class="sxs-lookup"><span data-stu-id="bb82f-112">PARAMETERS</span></span>

### <span data-ttu-id="bb82f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb82f-113">-DefaultProfile</span></span>
<span data-ttu-id="bb82f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb82f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb82f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb82f-115">-Name</span></span>
<span data-ttu-id="bb82f-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="bb82f-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb82f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb82f-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb82f-118">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="bb82f-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb82f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb82f-119">-ResourceId</span></span>
<span data-ttu-id="bb82f-120">A ID do recurso da conta ANF</span><span class="sxs-lookup"><span data-stu-id="bb82f-120">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb82f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb82f-121">CommonParameters</span></span>
<span data-ttu-id="bb82f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb82f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb82f-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb82f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb82f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb82f-124">INPUTS</span></span>

### <span data-ttu-id="bb82f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bb82f-125">System.String</span></span>

## <span data-ttu-id="bb82f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb82f-126">OUTPUTS</span></span>

### <span data-ttu-id="bb82f-127">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bb82f-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bb82f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb82f-128">NOTES</span></span>

## <span data-ttu-id="bb82f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb82f-129">RELATED LINKS</span></span>
