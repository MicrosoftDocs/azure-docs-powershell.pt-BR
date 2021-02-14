---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 022093b8fe1df28a151405a18009b40dd24b0c97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116572"
---
# <span data-ttu-id="50fa0-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="50fa0-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="50fa0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="50fa0-103">Criar um objeto na memória para a Extensão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="50fa0-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="50fa0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50fa0-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="50fa0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="50fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="50fa0-106">Criar um objeto na memória para a Extensão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="50fa0-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="50fa0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="50fa0-107">EXAMPLES</span></span>

### <span data-ttu-id="50fa0-108">Exemplo 1: Criar objeto de extensão de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="50fa0-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="50fa0-109">Esse comando cria um objeto de extensão de área de trabalho remota que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="50fa0-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="50fa0-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="50fa0-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="50fa0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50fa0-111">PARAMETERS</span></span>

### <span data-ttu-id="50fa0-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="50fa0-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="50fa0-113">Atualizar automaticamente a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="50fa0-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fa0-114">-Credencial</span><span class="sxs-lookup"><span data-stu-id="50fa0-114">-Credential</span></span>
<span data-ttu-id="50fa0-115">Credencial para Extensão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="50fa0-115">Credential for Remote Desktop Extension.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fa0-116">-Expiração</span><span class="sxs-lookup"><span data-stu-id="50fa0-116">-Expiration</span></span>
<span data-ttu-id="50fa0-117">Expiração da Extensão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="50fa0-117">Expiration for Remote Desktop Extension.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fa0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="50fa0-118">-Name</span></span>
<span data-ttu-id="50fa0-119">Nome da Extensão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="50fa0-119">Name of Remote Desktop Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fa0-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="50fa0-120">-RolesAppliedTo</span></span>
<span data-ttu-id="50fa0-121">Funções aplicadas a.</span><span class="sxs-lookup"><span data-stu-id="50fa0-121">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fa0-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="50fa0-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="50fa0-123">Versão da Extensão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="50fa0-123">Remote Desktop Extension version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fa0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fa0-124">CommonParameters</span></span>
<span data-ttu-id="50fa0-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50fa0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fa0-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50fa0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fa0-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="50fa0-127">INPUTS</span></span>

## <span data-ttu-id="50fa0-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="50fa0-128">OUTPUTS</span></span>

### <span data-ttu-id="50fa0-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="50fa0-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="50fa0-130">Notas</span><span class="sxs-lookup"><span data-stu-id="50fa0-130">NOTES</span></span>

<span data-ttu-id="50fa0-131">Aliases</span><span class="sxs-lookup"><span data-stu-id="50fa0-131">ALIASES</span></span>

## <span data-ttu-id="50fa0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50fa0-132">RELATED LINKS</span></span>

