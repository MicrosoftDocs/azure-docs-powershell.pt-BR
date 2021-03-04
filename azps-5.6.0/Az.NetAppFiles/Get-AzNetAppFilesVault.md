---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: d2741b3eb10618b9bdbe2e97b14d176c2b3eab26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887454"
---
# <span data-ttu-id="82e05-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="82e05-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="82e05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e05-102">SYNOPSIS</span></span>
<span data-ttu-id="82e05-103">Obtém a lista de cofres de backup de contas do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="82e05-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="82e05-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="82e05-104">SYNTAX</span></span>

### <span data-ttu-id="82e05-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="82e05-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82e05-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e05-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82e05-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e05-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82e05-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="82e05-108">DESCRIPTION</span></span>
<span data-ttu-id="82e05-109">O cmdlet **Get-AzNetAppFilesVault** obtém uma lista de cofres de backup de contas ANF.</span><span class="sxs-lookup"><span data-stu-id="82e05-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="82e05-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82e05-110">EXAMPLES</span></span>

### <span data-ttu-id="82e05-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="82e05-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="82e05-112">Este comando obtém uma lista dos cofres de backup da conta "MyAnfAccount" do Azure NetappFiles (ANF).</span><span class="sxs-lookup"><span data-stu-id="82e05-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="82e05-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="82e05-113">PARAMETERS</span></span>

### <span data-ttu-id="82e05-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82e05-114">-AccountName</span></span>
<span data-ttu-id="82e05-115">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="82e05-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e05-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="82e05-116">-AccountObject</span></span>
<span data-ttu-id="82e05-117">A conta do novo objeto de backup</span><span class="sxs-lookup"><span data-stu-id="82e05-117">The account for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82e05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e05-118">-DefaultProfile</span></span>
<span data-ttu-id="82e05-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="82e05-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82e05-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e05-120">-ResourceGroupName</span></span>
<span data-ttu-id="82e05-121">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="82e05-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="82e05-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82e05-122">-ResourceId</span></span>
<span data-ttu-id="82e05-123">A id de recurso do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="82e05-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="82e05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e05-124">CommonParameters</span></span>
<span data-ttu-id="82e05-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82e05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e05-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82e05-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e05-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82e05-127">INPUTS</span></span>

### <span data-ttu-id="82e05-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="82e05-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="82e05-129">System.String</span><span class="sxs-lookup"><span data-stu-id="82e05-129">System.String</span></span>

## <span data-ttu-id="82e05-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="82e05-130">OUTPUTS</span></span>

### <span data-ttu-id="82e05-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="82e05-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="82e05-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="82e05-132">NOTES</span></span>

## <span data-ttu-id="82e05-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82e05-133">RELATED LINKS</span></span>
