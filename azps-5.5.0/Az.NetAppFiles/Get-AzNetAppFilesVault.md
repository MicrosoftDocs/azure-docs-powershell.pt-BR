---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118403"
---
# <span data-ttu-id="8e33b-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="8e33b-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="8e33b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e33b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e33b-103">Obtém uma lista dos cofres de backup de Contas do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="8e33b-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="8e33b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e33b-104">SYNTAX</span></span>

### <span data-ttu-id="8e33b-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e33b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e33b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e33b-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e33b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e33b-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e33b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e33b-108">DESCRIPTION</span></span>
<span data-ttu-id="8e33b-109">O **cmdlet Get-AzNetAppFilesVault obtém** uma lista de cofres de backup de contas ANF.</span><span class="sxs-lookup"><span data-stu-id="8e33b-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="8e33b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e33b-110">EXAMPLES</span></span>

### <span data-ttu-id="8e33b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e33b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="8e33b-112">Esse comando obtém uma lista dos cofres de backup da conta do Azure NetappFiles (ANF) "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="8e33b-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="8e33b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e33b-113">PARAMETERS</span></span>

### <span data-ttu-id="8e33b-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="8e33b-114">-AccountName</span></span>
<span data-ttu-id="8e33b-115">O nome da conta da ANF</span><span class="sxs-lookup"><span data-stu-id="8e33b-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="8e33b-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8e33b-116">-AccountObject</span></span>
<span data-ttu-id="8e33b-117">A conta do novo objeto de backup</span><span class="sxs-lookup"><span data-stu-id="8e33b-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="8e33b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e33b-118">-DefaultProfile</span></span>
<span data-ttu-id="8e33b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e33b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e33b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e33b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8e33b-121">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="8e33b-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8e33b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e33b-122">-ResourceId</span></span>
<span data-ttu-id="8e33b-123">A ID do recurso do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="8e33b-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="8e33b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e33b-124">CommonParameters</span></span>
<span data-ttu-id="8e33b-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e33b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e33b-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e33b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e33b-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e33b-127">INPUTS</span></span>

### <span data-ttu-id="8e33b-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8e33b-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8e33b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8e33b-129">System.String</span></span>

## <span data-ttu-id="8e33b-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e33b-130">OUTPUTS</span></span>

### <span data-ttu-id="8e33b-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8e33b-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="8e33b-132">Notas</span><span class="sxs-lookup"><span data-stu-id="8e33b-132">NOTES</span></span>

## <span data-ttu-id="8e33b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e33b-133">RELATED LINKS</span></span>
