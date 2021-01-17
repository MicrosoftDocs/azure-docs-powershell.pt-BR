---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427063"
---
# <span data-ttu-id="de2aa-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="de2aa-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="de2aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="de2aa-103">Obtém a lista de cofres de backup de contas do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="de2aa-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="de2aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de2aa-104">SYNTAX</span></span>

### <span data-ttu-id="de2aa-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="de2aa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de2aa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de2aa-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de2aa-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de2aa-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de2aa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de2aa-108">DESCRIPTION</span></span>
<span data-ttu-id="de2aa-109">O cmdlet **Get-AzNetAppFilesVault** Obtém uma lista de cofres de backup de contas do ANF.</span><span class="sxs-lookup"><span data-stu-id="de2aa-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="de2aa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de2aa-110">EXAMPLES</span></span>

### <span data-ttu-id="de2aa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de2aa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="de2aa-112">Esse comando obtém uma lista dos cofres de backup da conta do Azure NetappFiles (ANF) "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="de2aa-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="de2aa-113">OS</span><span class="sxs-lookup"><span data-stu-id="de2aa-113">PARAMETERS</span></span>

### <span data-ttu-id="de2aa-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de2aa-114">-AccountName</span></span>
<span data-ttu-id="de2aa-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="de2aa-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="de2aa-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="de2aa-116">-AccountObject</span></span>
<span data-ttu-id="de2aa-117">A conta para o novo objeto de backup</span><span class="sxs-lookup"><span data-stu-id="de2aa-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="de2aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2aa-118">-DefaultProfile</span></span>
<span data-ttu-id="de2aa-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de2aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de2aa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de2aa-120">-ResourceGroupName</span></span>
<span data-ttu-id="de2aa-121">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="de2aa-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="de2aa-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de2aa-122">-ResourceId</span></span>
<span data-ttu-id="de2aa-123">A ID do recurso do pool ANF</span><span class="sxs-lookup"><span data-stu-id="de2aa-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="de2aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2aa-124">CommonParameters</span></span>
<span data-ttu-id="de2aa-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de2aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de2aa-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de2aa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2aa-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de2aa-127">INPUTS</span></span>

### <span data-ttu-id="de2aa-128">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="de2aa-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="de2aa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="de2aa-129">System.String</span></span>

## <span data-ttu-id="de2aa-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de2aa-130">OUTPUTS</span></span>

### <span data-ttu-id="de2aa-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="de2aa-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="de2aa-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de2aa-132">NOTES</span></span>

## <span data-ttu-id="de2aa-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de2aa-133">RELATED LINKS</span></span>
